# Licensing

This page explains, in plain language, what you may do with OmniScale. The
binding text is the [GNU General Public License, version 3](https://www.gnu.org/licenses/gpl-3.0.en.html)
or any later version, a copy of which is included with every build.

## The short version

**OmniScale is free software.** Not free of charge — free as in you own what
you receive. If you have a copy, you may use it for anything, study how it
works, change it, and pass it on.

**OmniScale is also donationware.** It is not on any store, and the only way
to get a build is from the people who make it, through Ko-fi or Patreon.

Those two facts are not in conflict, and it is worth being precise about why.

## Why OmniScale is GPL

This is not an accident of copying a license file. OmniScale is a modified
version of [DLSS Swapper](https://github.com/beeradmoore/dlss-swapper) by
Brad Moore — taken from v1.2.5.0 in August 2026 and substantially rewritten
and extended since. DLSS Swapper is itself GPL-3.0, and a great deal of its
game-library detection, manifest format and translation system is still
Brad Moore's code. A modified version of GPL-3.0 software is GPL-3.0 as a
whole; there is no way to change that by choosing a different license file.

## What this means if you support the project

You receive the packaged build **and** the complete corresponding source, as
the license requires. Concretely, you may:

- Install it on as many of your own machines as you like.
- Read the source and satisfy yourself that it does what this page claims.
- Modify it for your own use.
- Give copies to other people, including for free.

You do **not** owe anyone permission to do these things, and nothing you
agree to when donating takes them away. If any statement anywhere — on
Patreon, on Ko-fi, or in this repository — appears to contradict the GPL,
**the GPL wins**.

## Then what is the donation for?

For the work, and for the convenience.

Building OmniScale yourself is possible: install the .NET and Windows App
SDK toolchain, restore the solution, and publish it. Supporting the project
means someone else keeps doing that as game launchers, driver behavior and
upstream DLSS Swapper change, tracks new upscaler runtimes as vendors ship
them, and answers you when something breaks.

That is what is being sold: **time and continuity, not permission.**

## What is not covered by the GPL

The GPL covers the software. It does not cover names and logos.

The name **OmniScale**, its icon, the **OmniVex** identity, and the
associated visual design are not licensed to you by the GPL. You may fork
the code freely — but a fork must carry its own name and its own icon.
Details: [TRADEMARK.md](TRADEMARK.md).

## A request, not a restriction

Because OmniScale is GPL, nothing stops you from taking a build you received
and republishing it for free. That is your right and it will not be
contested. The project simply asks that you don't, because donationware only
works while the people who benefit from it choose to support it. If you
can't afford to contribute, ask instead of quietly passing a copy around —
email **andre.hetzl@gmail.com** and you'll get one.

## Upstream DLSS Swapper is a separate project

OmniScale is a fork, not a rebrand. Its issue tracker, wiki and releases are
Brad Moore's, and nothing in OmniScale files anything there — every "report
a problem" route in this app points at OmniScale's own maintainer instead.
Full attribution: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
