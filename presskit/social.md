<!--
Ready-to-paste launch copy for social platforms. Replace KOFI_LINK /
PATREON_LINK with the real URLs before posting. Screenshot filenames refer
to assets/screenshots/*.png.
-->

## Micro (X/Bluesky, under 280 characters)

> OmniScale: one Windows app for the upscaler DLLs a game ships with. Swap
> DLSS/FSR/XeSS versions, manage OptiScaler and DLSS Enabler, get the
> truth about what FSR 4 actually needs. Free software, donationware, not
> on any store. KOFI_LINK

(224 characters, room to spare for a link shortener or hashtag.)

**Screenshot:** `games-library.png` -- the game grid, upscaler status on
every real tile.

---

## Short (Mastodon, Bluesky long post)

> OmniScale is a Windows app that manages the upscaler DLLs your games
> ship with -- DLSS, FSR 3.1/4, XeSS -- swap versions, install OptiScaler or
> DLSS Enabler through one shared shim slot, and track whole runtime sets
> like NVIDIA Streamline and AMD's FidelityFX SDK 2. Every write is
> signature-checked, every swap keeps a backup, and it tells you the truth
> about FSR 4: that's a driver feature, not a file. Free software
> (GPL-3.0) and donationware -- supported directly by the people who use
> it. KOFI_LINK / PATREON_LINK

**Screenshot:** `runtime-versions.png` -- every DLSS/FSR/XeSS version
OmniScale tracks, FSR 4 on its own tab. Concrete, and it shows the product
doing the thing rather than a marketing frame.

---

## Medium (Reddit self-post opener, LinkedIn)

> I've spent the last stretch building OmniScale, a Windows app for
> managing the upscaler runtimes your games ship with. It started as a
> fork of DLSS Swapper and grew from there: FSR 3.1/4 and XeSS tracking
> alongside DLSS, a shared-slot manager for OptiScaler and DLSS Enabler so
> the two can't collide, whole-runtime-set updates for NVIDIA Streamline
> and AMD's FidelityFX SDK 2, and drift detection when a game update
> reverts a swap you made.
>
> It's also honest about where it can't help: FSR 4 lives in the AMD
> driver, not in any file a game ships, so OmniScale reports what's
> present and leaves the actual verdict to your hardware -- it doesn't
> claim to switch on something no file-swapping tool controls.
>
> It's free software (GPL-3.0, since DLSS Swapper is) and donationware --
> not sold outright, supported directly through Ko-fi or Patreon.
> Installation instructions and the full writeup are in the repo.

**Screenshot:** `games-library.png` -- 351 real games detected across seven
launchers, shows the detection claim isn't just a README number.

---

## Long (forum announcement, changelog post)

> **OmniScale -- one Windows app for the upscaler runtimes your games
> ship with.**
>
> The pitch: see what's in each game, swap it for a different version,
> and put the original back -- per game, with backups and a record of
> every write. DLSS, DLSS Frame Generation, DLSS Ray Reconstruction, AMD
> FSR 3.1, and Intel XeSS up through Frame Generation and XeLL, all
> tracked with the full four-part version number, not a folder-name
> guess.
>
> Underneath: OptiScaler and DLSS Enabler share one shim slot so the two
> can't collide, tracked file-by-file with exact rollback. Whole runtime
> sets -- NVIDIA Streamline's eleven DLLs, AMD's FidelityFX SDK 2, Direct
> Storage, the Direct3D 12 Agility SDK -- update all-or-nothing. Games are
> found automatically across Steam, GOG, Epic, Ubisoft Connect, Xbox,
> Battle.net and EA, plus any folder you point it at. NTFS transparent
> compression gets disk space back per game, in batches.
>
> It's honest about its limits, too. FSR 4 is an AMD driver feature -- no
> file-swapping tool, this one included, can turn it on by copying DLLs.
> OmniScale reports which FidelityFX shape a game carries and whether AMD
> hardware is present, and leaves the verdict to the driver instead of
> claiming one.
>
> It's free software -- GPL-3.0, since it's a modified version of DLSS
> Swapper -- and donationware: not sold outright, not on any store. Builds
> go directly to supporters through Ko-fi (KOFI_LINK) or Patreon
> (PATREON_LINK), and if you can't support it right now, ask anyway --
> you'll get a copy. See docs/INSTALL.md in the repo for setup.

**Screenshot:** a two-up of `games-library.png` and `runtime-versions.png`
-- shows both the everyday view (your library, upscaler status at a
glance) and the depth underneath (every tracked runtime version, FSR 4
included) in a single image.
