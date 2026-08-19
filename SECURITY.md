# Security Policy

OmniScale writes files into your game folders and, for OptiScaler and DLSS
Enabler, downloads and runs third-party binaries on your machine. That
combination — file replacement with real consequences if it goes wrong, and
installing code OmniScale itself didn't write — is exactly the kind of thing
that deserves a place to report problems.

## Scope

In scope:

- The app itself: file swapping, the DLL catalogue and download path,
  OptiScaler/DLSS Enabler install and shim-slot management, the setup and
  uninstall flow, and anything touching your app data or your game files.
- The installer and portable build, and the update path between versions.
- Authenticode signature verification on downloaded/replaced files.

Out of scope:

- OptiScaler's and DLSS Enabler's own internals — report issues with those
  tools to their own maintainers, linked in
  [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
- DLSS Swapper's upstream manifest and download infrastructure — OmniScale
  reads it but does not operate it.
- Anti-cheat bans resulting from using OptiScaler or DLSS Enabler in a
  multiplayer game with kernel-level anti-cheat. OmniScale warns about this
  and requires a typed confirmation before proceeding; the risk itself is
  not a vulnerability in OmniScale.

## How to report

Email **andre.hetzl@gmail.com** with a description of the issue, your
Windows version, and, if possible, steps to reproduce. Please do not open a
public GitHub issue for a vulnerability that isn't already public — this is
currently a single-maintainer project with no dedicated security mailing
list or bug-bounty program, so a direct email is the fastest path to a fix.

## What to expect

There's no SLA — this is a single-maintainer, unpaid project — but a
genuine security report will get a response acknowledging receipt, and a
fix will be prioritized over feature work once confirmed. If you don't hear
back within a couple of weeks, it's fine to follow up; it does not mean the
report was ignored on purpose.

## Trust model

Being explicit about what OmniScale treats as trusted versus untrusted:

- **Every file OmniScale writes into a game folder** — a swapped DLL, an
  OptiScaler or DLSS Enabler install — is checked against its Authenticode
  signature first. A file that fails verification is not written.
- **The original file is always kept** before a swap, so "put it back" is a
  real operation on a real backup, not a re-download and a guess.
- **Nothing is installed silently.** OptiScaler and DLSS Enabler both
  require an explicit, typed confirmation before OmniScale touches a
  multiplayer game with kernel-level anti-cheat present.
- **Uninstall restores exactly what was replaced**, tracked file by file —
  not a best-effort cleanup.
- **App data is never purged by an update.** A dedicated policy
  (`AppDataPurgePolicy`) only allows the uninstall path to remove your
  settings, database and downloaded files, and only when it can positively
  verify it is running from the machine's actual registered install
  location — not merely because a flag says "this is real." A pre-update
  database backup is kept as a second line of defense.

If you find a gap in any of the above — a case where an unsigned or
unverified file gets written, or a place this document's claims don't match
what OmniScale actually does — that is exactly the kind of report this
policy exists for.
