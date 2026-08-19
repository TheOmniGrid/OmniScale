# Third-party notices

OmniScale is built on other people's work, under their own licenses. This
file credits every one of them — the same list the app's own Credits &
Licences screen shows, with the license texts in full. If you redistribute
OmniScale, this file must travel with it — see [LICENSING.md](LICENSING.md).

## The project this is built on

**[DLSS Swapper](https://github.com/beeradmoore/dlss-swapper) by Brad Moore,
GPL-3.0.** OmniScale is a modified version of DLSS Swapper, taken from
v1.2.5.0 in August 2026 and substantially rewritten and extended since. Its
game-library detection, manifest format, download plumbing and translation
system started there, and a great deal of that code is still Brad Moore's.
Two consequences worth stating plainly:

- **The DLL catalogue and the file server are still upstream's.** OmniScale
  reads DLSS Swapper's manifest (`beeradmoore.github.io/dlss-swapper`) and
  downloads runtimes and cover art from `dlss-swapper-downloads.beeradmoore.com`.
  It runs no CDN of its own, so if that host changes, OmniScale's DLL
  downloads stop until it is pointed elsewhere.
- **Upstream is not where OmniScale problems go.** Their issue tracker,
  wiki, subreddit and winget package are theirs. Nothing in this app files
  anything there; every "something is wrong" route in OmniScale points at
  its own log file and its own maintainer instead.

## Tools OmniScale installs or learned from

- **[OptiScaler](https://github.com/optiscaler/OptiScaler)** by cdozdil and
  contributors, GPL-3.0 — the translation layer OmniScale downloads and
  installs so a game that asks for one upscaler can receive another. Itself
  descended from [CyberFSR2](https://github.com/PotatoOfDoom/CyberFSR2).
- **[DLSS Enabler](https://www.nexusmods.com/site/mods/757)** by
  artur-graniszewski — frame generation in titles that never shipped it.
  OmniScale downloads the author's own package, via the Nexus Mods API and
  an API key you provide yourself.
- **[DLSSTweaks](https://github.com/emoose/DLSSTweaks)** by emoose, MIT —
  where the idea came from that DLSS is worth *configuring*: forced DLAA,
  preset overrides, the on-screen indicator. OmniScale implements these
  itself rather than shipping DLSSTweaks' code.
- **[CompactGUI](https://github.com/IridiumIO/CompactGUI)** by IridiumIO,
  GPL-3.0 — credited for the idea, not for code: that per-game transparent
  compression deserves a real interface.

## Vendor SDKs

[NVIDIA Streamline](https://github.com/NVIDIA-RTX/Streamline),
[AMD FidelityFX SDK](https://github.com/GPUOpen-LibrariesAndSDKs/FidelityFX-SDK),
[Intel XeSS](https://github.com/intel/xess), and Microsoft's DirectStorage
and Direct3D 12 Agility SDK redistributables. Each ships under its own
vendor license, reproduced in full on the app's Credits & Licences screen.

## Corrections

If any license attribution here is wrong or has changed upstream, please
[open an issue](../../issues/new/choose) or email
**andre.hetzl@gmail.com** — this file is only as good as its last
verification, and getting it right matters more than getting it fast.
