# Changelog

All notable changes to OmniScale are recorded here, most recent first.

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
