# Frequently asked questions

Short, direct answers. If your question isn't here, [open an
issue](https://github.com/TheOmniGrid/OmniScale/issues/new/choose).

## Why isn't this on a store?

There isn't really a "store" for this kind of tool — OmniScale is a
standalone Windows app, not a browser extension. It's donationware: builds
go directly to supporters through Ko-fi or Patreon rather than being handed
out for free from a public download page. See [Get OmniScale](README.md#get-omniscale).

## Is it really free software if I donate for it?

Yes. OmniScale is GPL-3.0, because it's a modified version of
[DLSS Swapper](https://github.com/beeradmoore/dlss-swapper), which is
GPL-3.0 itself. Anyone who has a copy — donor or not — gets the full source
and every right the GPL grants: use it, study it, modify it, share it. The
donation buys convenience and continuity, not permission. Full detail:
[LICENSING.md](LICENSING.md).

## Can I share my copy?

Yes — the GPL guarantees it, and doing so will not be contested. The
project simply asks that you don't, because donationware only works while
the people who benefit from it choose to support it. If you can't afford to
contribute, ask instead of quietly passing a copy around — you'll get one.

## How is this different from DLSS Swapper?

OmniScale started as a fork of DLSS Swapper and has since diverged
substantially: FSR 3.1/4 and XeSS runtime tracking (not just DLSS), a
shared-shim-slot OptiScaler/DLSS Enabler manager, NVIDIA Streamline and AMD
FidelityFX SDK 2 set updates, DirectStorage/Agility SDK tracking, NTFS
transparent compression, drift detection when a game update reverts a swap,
and honest reporting on what FSR 4 actually requires (the driver, not a
file). The game-library detection, manifest format and translation
plumbing underneath still trace back to DLSS Swapper — see
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## Does OmniScale actually turn on FSR 4?

No, and it says so rather than pretending otherwise. FSR 4 is an AMD driver
feature, not something any file-swapping tool can enable. OmniScale reports
which FidelityFX shape a game carries — the older FSR 3.1 monolith, or the
newer SDK 2 set that can reach FSR 4 — and whether AMD hardware is present,
and leaves the actual verdict to your driver.

## What data do you collect?

None, from OmniScale's side — no telemetry, no analytics, no crash
reporting, no account. OmniScale does talk to the network, though: it
downloads DLLs, mods and version listings from the hosts that provide them.
Full detail, including exactly which hosts and why: [PRIVACY.md](PRIVACY.md).

## Is it safe to swap these DLLs?

Every file OmniScale writes is checked against its Authenticode signature
first — an unsigned or wrong-signature file is not written. The original is
always kept, so a bad swap is a one-click revert, not a reinstall. That
said: swapping can fix visual artifacts, change nothing, or in rare cases
stop a game launching until you press Reset. OmniScale can't promise a
newer runtime is a better one for every game.

## Will I get banned for using OptiScaler or DLSS Enabler?

Possibly, in a multiplayer game with kernel-level anti-cheat — installing
either tool modifies files that anti-cheat software may flag. OmniScale
requires a typed confirmation before doing this in a game it recognizes as
having kernel-level anti-cheat. The risk is real and it's yours; OmniScale
can only warn you about it, not remove it.

## What happens when I update OmniScale?

Installing a new version over an existing install never touches your
settings, database, or downloaded files — that's enforced by a dedicated
policy, not just documentation, and it's backstopped by a pre-update
database backup as a second safety net. Uninstalling, on the other hand,
still removes everything by design — export or back up first if you might
want the app data back.

## What happens if the project stops?

The GPL means the source doesn't stop existing along with the project —
anyone who has a copy keeps every right to it, including the right to fork
it under a new name and icon (see [TRADEMARK.md](TRADEMARK.md)). What
would stall is tracking new upscaler runtimes as vendors ship them — DLLs
already in the catalogue keep working exactly as they do today.
