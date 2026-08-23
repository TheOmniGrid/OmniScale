# OmniScale Privacy Policy

**Effective date:** 2026-08-24
**Contact:** andre.hetzl@gmail.com

## Summary

OmniScale has no telemetry, no analytics, no crash reporting, and no account
of its own. It does not know who you are and does not try to find out.
Unlike a browser extension, though, OmniScale's whole job involves talking
to the network — downloading the DLLs and mods it manages — so this page is
about being specific regarding that traffic, not claiming there isn't any.

## What is stored locally, and where

Everything OmniScale remembers lives in `StoredData\` next to the portable
build, or in your per-user app data folder for the installed version:
your library database, settings, downloaded runtime files, cover art cache,
and — if you provide one — your Nexus Mods API key. None of it is synced to
any OmniScale server, because no such server exists.

One exception worth naming: if a game page plays a trailer (see below), the
embedded player is a real browser engine (WebView2) and keeps its own
browser profile — including whatever cookies YouTube sets — in a `WebView2`
folder inside your temp directory. Deleting that folder clears it.

## What OmniScale contacts, and why

**Always, as part of its core job:**

| Host | Purpose |
|---|---|
| `beeradmoore.github.io/dlss-swapper` | The DLL catalogue manifest — what runtime versions exist and where to get them. Upstream DLSS Swapper's own manifest; OmniScale runs no CDN of its own. |
| `dlss-swapper-downloads.beeradmoore.com` | The runtime DLLs themselves, and game cover art. |
| `ngx.download.nvidia.com` | NVIDIA's own distribution host, contacted directly for certain NVIDIA-hosted assets. |
| `api.nuget.org` | Public version listings for the DirectStorage and Direct3D 12 Agility SDK NuGet packages. |
| `api.github.com` | Public release listings for OptiScaler and DLSS Enabler, so OmniScale knows what the current version is. |
| Your game stores' own art hosts | Cover art for detected games, fetched from whichever store the game came from (Steam, GOG, Epic, Ubisoft and Battle.net all serve their own artwork). |

**Only if you supply the matching API key in Settings.** OmniScale ships no
keys of its own, so with none configured none of these are ever contacted:

| Host | Purpose |
|---|---|
| `api.nexusmods.com` | Your Nexus Mods key, to check for and download DLSS Enabler updates. Authenticated with **your** key — Nexus Mods sees your account making the request, the same as if you downloaded the file yourself in a browser. |
| `api.igdb.com`, `id.twitch.tv`, `images.igdb.com` | Your IGDB credentials (IGDB authenticates through Twitch), for better cover art, and for the game descriptions and trailer links shown on a game's page. |
| `www.steamgriddb.com` | Your SteamGridDB key, for community cover art. |
| `api.rawg.io` | Your RAWG key, as a further cover-art source. |

**The trailer player, and what makes it different:**

| Host | Purpose |
|---|---|
| `www.youtube.com` and the Google hosts it loads from | When a game's page has found a trailer, it plays one, muted and looping, inside an embedded YouTube player. |

This one deserves singling out, because it is the only place OmniScale loads
**someone else's web page** rather than fetching a file: YouTube and Google
see the request the same way they would if you opened that video in a
browser tab, and they may set cookies in the player's own profile described
above. It only happens when a trailer was found for that game, which
requires IGDB credentials — with no IGDB key configured, no trailer is ever
looked up and YouTube is never contacted. Opening a game's page is what
starts it; the library grid never does.

Apart from that player, every request above is for **public data OmniScale
needs to do its job** — a manifest, a file, a version number. None of them
carry your settings, your game library, or any identifier beyond what any
plain HTTP request necessarily includes (your IP address, as seen by that
server).

## What OmniScale never does

- No telemetry, analytics, or crash reports, to us or anyone else.
- No account, no sign-in, no server of OmniScale's own.
- It never downloads `nvngx_dlss.dll` on your behalf — NVIDIA's license
  doesn't permit redistributing it, so OmniScale doesn't try.
- It never writes to a game folder without a signature check passing first,
  and never installs OptiScaler or DLSS Enabler into a multiplayer game
  with kernel-level anti-cheat without an explicit, typed confirmation.

## Your API keys

If you add any of them — Nexus Mods, IGDB, SteamGridDB, RAWG — each is
stored locally, used only to authenticate the requests listed above, and
never sent anywhere except the service it belongs to. Removing one in
Settings deletes it from local storage; OmniScale keeps no copy anywhere
else, and has no keys of its own to fall back on.

## Changes to this policy

If OmniScale's network behavior changes, this document will be updated and
the effective date above will change with it.

## Contact

Questions about this policy: **andre.hetzl@gmail.com**
