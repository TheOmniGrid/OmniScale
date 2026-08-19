# OmniScale Privacy Policy

**Effective date:** 2026-08-19
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

## What OmniScale contacts, and why

| Host | Purpose |
|---|---|
| `beeradmoore.github.io/dlss-swapper` | The DLL catalogue manifest — what runtime versions exist and where to get them. Upstream DLSS Swapper's own manifest; OmniScale runs no CDN of its own. |
| `dlss-swapper-downloads.beeradmoore.com` | The runtime DLLs themselves, and game cover art. |
| `ngx.download.nvidia.com` | NVIDIA's own distribution host, contacted directly for certain NVIDIA-hosted assets. |
| `api.nuget.org` | Public version listings for the DirectStorage and Direct3D 12 Agility SDK NuGet packages. |
| `api.github.com` | Public release listings for OptiScaler and DLSS Enabler, so OmniScale knows what the current version is. |
| `api.nexusmods.com` | Only if you add your own Nexus Mods API key in Settings, to check for and download DLSS Enabler updates. Requests are authenticated with **your** key, not one of OmniScale's — Nexus Mods sees your account making the request, the same as if you downloaded the file yourself in a browser. |

Every one of these is a request for **public data OmniScale needs to do its
job** — a manifest, a file, a version number. None of them carry your
settings, your game library, or any identifier beyond what any plain HTTP
request necessarily includes (your IP address, as seen by that server).

## What OmniScale never does

- No telemetry, analytics, or crash reports, to us or anyone else.
- No account, no sign-in, no server of OmniScale's own.
- It never downloads `nvngx_dlss.dll` on your behalf — NVIDIA's license
  doesn't permit redistributing it, so OmniScale doesn't try.
- It never writes to a game folder without a signature check passing first,
  and never installs OptiScaler or DLSS Enabler into a multiplayer game
  with kernel-level anti-cheat without an explicit, typed confirmation.

## Your Nexus Mods API key

If you add one, it is stored locally, used only to authenticate the
requests listed above, and never sent anywhere except `api.nexusmods.com`.
Removing it from Settings deletes it from local storage; OmniScale keeps no
copy anywhere else.

## Changes to this policy

If OmniScale's network behavior changes, this document will be updated and
the effective date above will change with it.

## Contact

Questions about this policy: **andre.hetzl@gmail.com**
