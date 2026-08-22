<p align="center">
  <img src="assets/banner-wide.gif?v=20260822-symbol-reactor" alt="OmniScale — Perfect scale. Every game." width="100%">
</p>

<h1 align="center">OmniScale</h1>
<p align="center"><b>One Windows app for the upscaler runtimes a game ships with: see what's in each game, swap it for a different version, and put the original back.</b></p>
<p align="center">Part of the <a href="#the-omnivex-suite">OmniVex</a> suite.</p>

<p align="center">
  <a href="https://www.patreon.com/TheOmniGrid"><img alt="Get it on Patreon" src="https://img.shields.io/badge/Get%20it%20on-Patreon-FF424D?style=for-the-badge&logo=patreon&logoColor=white"></a>
  &nbsp;
  <a href="https://ko-fi.com/theomnigrid"><img alt="Get it on Ko-fi" src="https://img.shields.io/badge/Get%20it%20on-Ko--fi-FF5E5B?style=for-the-badge&logo=kofi&logoColor=white"></a>
</p>

<p align="center">
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0.0-8A7BFF?style=flat-square">
  <img alt="Platform" src="https://img.shields.io/badge/platform-Windows%2010%20%2F%2011-0078D4?style=flat-square&logo=windows&logoColor=white">
  <img alt="Languages" src="https://img.shields.io/badge/languages-EN%20·%20DE%20·%20ES%20·%20FR%20·%20RO-8A7BFF?style=flat-square">
  <img alt="Telemetry" src="https://img.shields.io/badge/telemetry-none-2EA043?style=flat-square">
  <img alt="License" src="https://img.shields.io/badge/license-GPL--3.0-6A5BDB?style=flat-square">
</p>

<!-- Quick navigation. These are clickable: each chip jumps to a section of this
     page, or to the document it names. Anchors are GitHub's own slugs for the
     headings below -- if a heading is renamed, its chip has to be renamed too. -->
<p align="center">
  <a href="#get-omniscale"><img alt="Get OmniScale" src="https://img.shields.io/badge/⬇%20Get%20OmniScale-8A7BFF?style=for-the-badge"></a>
  <a href="#what-it-does"><img alt="Features" src="https://img.shields.io/badge/Features-2B2545?style=for-the-badge"></a>
  <a href="#five-languages"><img alt="Languages" src="https://img.shields.io/badge/Languages-2B2545?style=for-the-badge"></a>
  <a href="#see-it"><img alt="Screenshots" src="https://img.shields.io/badge/Screenshots-2B2545?style=for-the-badge"></a>
  <a href="PRIVACY.md"><img alt="Privacy" src="https://img.shields.io/badge/Privacy-2B2545?style=for-the-badge"></a>
  <a href="#what-this-does-not-do"><img alt="Limitations" src="https://img.shields.io/badge/Limitations-2B2545?style=for-the-badge"></a>
  <a href="#requirements"><img alt="Requirements" src="https://img.shields.io/badge/Requirements-2B2545?style=for-the-badge"></a>
  <a href="INSTALLATION.md"><img alt="Installation" src="https://img.shields.io/badge/Installation-2B2545?style=for-the-badge"></a>
  <a href="FAQ.md"><img alt="FAQ" src="https://img.shields.io/badge/FAQ-2B2545?style=for-the-badge"></a>
  <a href="SUPPORT.md"><img alt="Support" src="https://img.shields.io/badge/Support-2B2545?style=for-the-badge"></a>
  <a href="CHANGELOG.md"><img alt="Changelog" src="https://img.shields.io/badge/Changelog-2B2545?style=for-the-badge"></a>
</p>

> [!IMPORTANT]
> **Documentation-only repository.** This public repository contains OmniScale documentation, approved artwork, and screenshots—not the application source tree, installer, binary releases, signing material, or private build infrastructure. Official distribution remains outside GitHub.

<p align="center">
  <img src="assets/screenshots/games-library.png" alt="OmniScale's game grid, 351 games detected across seven launchers" width="920">
</p>

---

## What it does

**Swap the upscaler DLLs.** DLSS, DLSS Frame Generation, DLSS Ray Reconstruction,
AMD FSR 3.1 (DirectX 12 and Vulkan), Intel XeSS up to XeSS 3, XeSS for DirectX 11,
XeSS Frame Generation and XeLL. Every file is checked against its Authenticode
signature before anything is written, the original is kept beside the
replacement, and one button puts it back.

**Read the full version.** `3.10.2.0`, not `3.10` — the whole four-part number,
taken from the file itself rather than guessed from a folder name.

**Manage the mods that add upscalers to games that never had them.**
[OptiScaler](https://github.com/optiscaler/OptiScaler) and
[DLSS Enabler](https://www.nexusmods.com/site/mods/757) share one shim slot,
so the two cannot collide. Installs are tracked file by file and uninstall
restores exactly what was replaced. OptiScaler's `.ini` is editable from a real
settings screen rather than a text editor.

**Update the runtime sets a game already carries.** NVIDIA Streamline (all
eleven `sl.*.dll`, replacing only the ones the game actually ships), the AMD
FidelityFX SDK 2 set that reaches FSR 4, Microsoft DirectStorage and the
Direct3D 12 Agility SDK. Set updates are all-or-nothing with an exact rollback.

**Tell you the truth about FSR 4.** The ML upscaler lives in the Adrenalin
driver, not in any file a game ships, so no tool can switch it on by copying
DLLs. OmniScale reports which FidelityFX shape a game has — the FSR 3.1
monolith or the SDK 2 set that can reach FSR 4 — and whether AMD hardware is
present, and leaves the verdict to the driver instead of claiming one.

**Know what your GPU is.** Dedicated, integrated, or a hybrid laptop — asked of
the WDDM kernel, not guessed from the adapter name.

**Find games nothing else finds.** Steam, GOG, Epic, Ubisoft Connect, Xbox,
Battle.net, EA, plus any folder you point it at.

**Get the disk space back.** NTFS transparent compression (XPRESS or LZX) per
game, in batches, with a re-optimise pass that catches the files a game update
left uncompressed.

**Tell you when a game changed underneath you.** An update that reverted your
swap is detected and offered back, one game at a time or across the whole
library at once.

## Five languages

English, Deutsch, Español, Français and Română — the complete interface, not
just the menus. OmniScale follows your Windows display language automatically.

## See it

<table>
<tr>
<td><img src="assets/screenshots/games-library.png" alt="Game grid"><br><sub><b>Games</b> — 351 games detected across seven launchers, upscaler status on every tile.</sub></td>
<td><img src="assets/screenshots/runtime-versions.png" alt="Runtime version library"><br><sub><b>Library</b> — every DLSS/FSR/XeSS runtime version OmniScale tracks, FSR 4 included, on its own tab.</sub></td>
</tr>
</table>

## What this does not do

It does not add DLSS to a game that doesn't support it — that's what
OptiScaler and DLSS Enabler are for, and they come with their own caveats. It
does not promise a newer DLL is a better one: swapping can fix artifacts,
change nothing, or stop a game launching until you press Reset. It never
downloads `nvngx_dlss.dll` on your behalf, because NVIDIA's license doesn't
allow redistributing it.

Do not put OptiScaler or DLSS Enabler into a multiplayer game with
kernel-level anti-cheat. OmniScale warns you and makes you type a
confirmation; the ban risk is still yours.

## Requirements

| | |
| --- | --- |
| OS | Windows 10 64-bit, build 19041 (20H1) or newer |
| GPU | Any. Some features need a specific vendor's hardware to have any effect. |
| Runtime | None. The build carries its own .NET and Windows App SDK. |

## Get OmniScale

OmniScale is **donationware**. It is not on any store, and it is not sold
outright — it's supported directly by the people who use it.

<p align="center">
  <a href="https://www.patreon.com/TheOmniGrid"><img src="assets/support-patreon.svg" height="64" alt="Support OmniScale on Patreon"></a>
  &nbsp;&nbsp;
  <a href="https://ko-fi.com/theomnigrid"><img src="assets/support-kofi.svg" height="64" alt="Support OmniScale on Ko-fi"></a>
</p>

Supporters get the packaged, ready-to-install build (installer or portable,
your choice), the complete source matching that exact build, and new releases
as they land.

What you're paying for is convenience and the ongoing work — **not**
exclusivity. OmniScale is GPL-3.0: everyone who receives a build receives the
source with it, along with every freedom that license grants.
[LICENSING.md](LICENSING.md) explains exactly what that means.

If you can't afford to give anything, that's genuinely fine — say so and
you'll get a copy anyway.

## Documentation

| | |
|---|---|
| [Installation](INSTALLATION.md) | Installer and portable setup |
| [Privacy](PRIVACY.md) | Local data, downloads and telemetry boundaries |
| [FAQ](FAQ.md) | Common detection, switching and compatibility questions |
| [Support](SUPPORT.md) | Useful reports, privacy redaction and contact routes |
| [Security](SECURITY.md) | Private vulnerability reporting |
| [Contributing](CONTRIBUTING.md) | Documentation and reproducible-report scope |
| [Changelog](CHANGELOG.md) | Release history |
| [Licensing](LICENSING.md) | GPL terms, distribution and source availability |
| [Third-party notices](THIRD-PARTY-NOTICES.md) | Upstream projects and vendor components |

## The OmniVex suite

OmniScale is one of a family of tools sharing a design language and a
philosophy — modern, fast, no telemetry:

**OmniTheme** · **OmniBlock** · **OmniCleaner** · **OmniAPO** · **OmniEQ** · **OmniPlay** · **OmniScale** · **OmniShade** · **OmniVisuals** · **OmniGPU** · **OmniWrappers**

<sub>**OmniWrappers** is four Direct3D compatibility installers — OmniDXVK, OmniDxWrapper, OmniVKD3D and OmniVoodoo2.</sub>

<sub>Tuned for framerate, mixed for headroom, sharp to the pixel. Donationware
tools for gamers and audiophiles — audio, graphics, and a bit of privacy too.</sub>

More at [github.com/TheOmniGrid](https://github.com/TheOmniGrid).

---

## Credit

OmniScale is a modified version of
**[DLSS Swapper](https://github.com/beeradmoore/dlss-swapper)** by **Brad Moore**,
GPL-3.0 — taken from v1.2.5.0 in August 2026 and substantially rewritten and extended
since. Its game-library detection, manifest format, download plumbing and translation
system started there, and a great deal of that code is still his.

**OmniScale is a fork, not a rebrand.** DLSS Swapper's issue tracker, wiki and releases
are Brad Moore's, and nothing in OmniScale files anything there — please don't report
OmniScale problems to it.

It also manages, without bundling, **[OptiScaler](https://github.com/optiscaler/OptiScaler)**
by cdozdil and contributors (GPL-3.0) and **DLSS Enabler** by artur-graniszewski. The
ideas behind two features are credited without their code: **DLSSTweaks** by emoose (MIT)
and **CompactGUI** by IridiumIO (GPL-3.0). NVIDIA Streamline, AMD FidelityFX, Intel XeSS,
Microsoft DirectStorage and the D3D12 Agility SDK each ship under their own vendor licence.

Full attribution in [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

**Licensing at a glance:** the software is GPL-3.0 — you get the source, and you may study,
modify and share it. The name, logo and OmniVex identity are not covered by that licence;
fork the code freely, but give the fork its own name.
[LICENSING.md](LICENSING.md) · [TRADEMARK.md](TRADEMARK.md)

---

## Contact

Use public channels only for information that is safe to share. Remove usernames, local paths,
account identifiers, licence data, and other personal information from screenshots and logs.

| Channel | Use |
|---|---|
| [GitHub Issues](../../issues/new/choose) | Reproducible bugs, compatibility reports, and documentation corrections |
| [GitHub Discussions](../../discussions) | Questions, ideas, and community support |
| [Security](SECURITY.md) | Private vulnerability reporting — never use a public issue |
| [Email](mailto:omnivex@theomnigrid.biz) | Private support, delivery, or licensing questions |

Support is best-effort. See [SUPPORT.md](SUPPORT.md) and [CONTRIBUTING.md](CONTRIBUTING.md)
for repository scope and reporting guidance.

---

<p align="center">
  <strong>OmniScale</strong><br>
  <a href="https://github.com/TheOmniGrid">The OmniGrid on GitHub</a> ·
  <a href="https://ko-fi.com/theomnigrid">Ko-fi</a> ·
  <a href="https://www.patreon.com/TheOmniGrid">Patreon</a><br><br>
  <sub>Copyright © 2026 OmniVex · GPL-3.0 · <a href="LICENSING.md">Licensing</a></sub><br>
  <sub>A modified version of <a href="https://github.com/beeradmoore/dlss-swapper">DLSS Swapper</a> by Brad Moore. NVIDIA, AMD and Intel are trademarks of their respective owners; OmniScale is not affiliated with them.</sub>
</p>
