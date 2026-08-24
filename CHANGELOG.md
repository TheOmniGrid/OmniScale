# Changelog

All notable changes to OmniScale are recorded here, most recent first.

## Unreleased

### Added
- A redesigned game page header: the game's own cover art at full size
  beside a wide banner, with the title, its details and the action buttons
  laid out down the side rather than crowded along the bottom.
- Autoplaying game trailers on a game's page — muted, looping, no controls,
  as atmosphere rather than something to interact with. Requires IGDB
  credentials in Settings; without them no trailer is looked up and nothing
  is contacted. **This is the only feature that loads an external web page
  by default**, so it is called out in [PRIVACY.md](PRIVACY.md).
- Game descriptions on a game's page: genre, release year, developer and
  publisher, and a short summary, from IGDB using the same credentials.
- A custom cover can now be picked from a local image file, not only from
  the online cover search.
- Battle.net pre-release products (betas, PTR and test builds) are labelled
  as such — a beta that shares its install folder with the real game now
  reads "Call of Duty (Beta)" instead of a second, identical "Call of Duty".

### Changed
- Cover art is cached at four times the previous resolution, so covers look
  sharp at the larger sizes the new game page uses. Existing games refetch
  their art once, on the next scan after updating.
- The game page's banner is now a deliberately blurred rendition of the
  cover rather than the cover stretched wide, which no longer looks
  low-resolution for games whose store art is small to begin with.
- The interface is now fully translated into **ten languages**: English,
  German, Spanish, French, Romanian, Russian, Simplified Chinese, Japanese,
  Korean and Turkish. The last five previously existed only in part and fell
  back to English for most of the interface.

### Fixed
- A library scan could restart itself while one was already running — for
  example when a store was switched on or off mid-scan — leaving the app
  unresponsive with a game count that never finished.
- Two colours in the title bar and one in the DLL picker did not follow the
  app's own palette.

## 1.0.0.0

The first release. A modified version of DLSS Swapper v1.2.5.0, substantially
rewritten and extended.

### Added
- DLL swapping for DLSS, DLSS Frame Generation, DLSS Ray Reconstruction, AMD
  FSR 3.1 (DirectX 12 and Vulkan), Intel XeSS up to XeSS 3, XeSS for
  DirectX 11, XeSS Frame Generation, and XeLL — with Authenticode signature
  verification before every write, an original-file backup, and one-click
  revert.
- OptiScaler and DLSS Enabler management sharing one shim slot, installed
  and removed file-by-file with exact rollback.
- Runtime-set updates: NVIDIA Streamline (all eleven `sl.*.dll`), the AMD
  FidelityFX SDK 2 set that reaches FSR 4, Microsoft DirectStorage, and the
  Direct3D 12 Agility SDK — all-or-nothing, with exact rollback.
- Honest FSR 4 reporting: which FidelityFX shape a game carries and whether
  AMD hardware is present, without claiming to switch on a driver feature no
  file-swapping tool can control.
- GPU identification via the WDDM kernel rather than adapter-name guessing.
- Cross-launcher game discovery: Steam, GOG, Epic, Ubisoft Connect, Xbox,
  Battle.net, EA, plus any custom folder.
- NTFS transparent compression per game, in batches, with a re-optimize pass.
- Drift detection: an update that reverts a swap is detected and offered
  back, per-game or library-wide.
- A full interface in English, German, Spanish, French and Romanian.

### Security
- Every file OmniScale writes is checked against its Authenticode signature
  first; a file that fails verification is not written.
- App data is protected from being purged by anything except a genuinely
  verified uninstall, checked positively against the machine's registered
  install location rather than an easily-unset flag — see
  [SECURITY.md](SECURITY.md).
- A pre-update database backup is kept automatically as a second line of
  defense against data loss across an update.
- Development and validation hooks (the sandboxed setup path used by this
  project's own test probes) are compiled out of shipped builds entirely —
  a release binary refuses them rather than silently ignoring them.
