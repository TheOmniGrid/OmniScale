# Installing OmniScale

OmniScale is not on any public download page — see
["Why isn't this on a store?"](FAQ.md#why-isnt-this-on-a-store) if you want
the reasoning. Supporters get one of two builds directly: an installer or a
portable zip. Haven't got a build yet? See
[Get OmniScale](README.md#get-omniscale) in the main README.

## Installer

`OmniScale-<version>-installer.exe` is the normal way to install OmniScale.

1. Run the installer. It needs administrator rights only to write to
   `Program Files`; OmniScale itself never runs elevated.
2. A setup window — drawn by OmniScale itself, not a generic installer
   dialog — asks where to install, copies the files, and creates a Start
   Menu shortcut and an uninstall entry.
3. Launch OmniScale from the Start Menu.

**About the SmartScreen warning.** Windows may show a "Windows protected
your PC" prompt the first time you run the installer. That's expected for
any app that isn't yet widely distributed enough to have built up
SmartScreen reputation — it isn't a sign anything is wrong. Click **More
info → Run anyway** if you trust the source you downloaded from.

### Updating

Run the new installer over the existing install — do **not** uninstall
first. Your settings, library database, and downloaded files are untouched
by an update: verified independently, not just documented, and backstopped
by an automatic pre-update database backup. See
["What happens when I update OmniScale?"](FAQ.md#what-happens-when-i-update-omniscale).

## Portable

`OmniScale-<version>-portable.zip` installs nothing.

1. Unzip it anywhere.
2. Run `OmniScale.exe`.

Everything OmniScale stores lives in `StoredData\` next to the executable,
so the whole folder can be moved or deleted as one unit. There is no
installer, no registry entry, and no elevation prompt.

### Updating

Unzip the new release over the old folder, or into a fresh folder and copy
`StoredData\` across yourself. Either way: your data lives in that one
folder, so treat it like any other folder you'd back up before a big
change.

## Verifying the install worked

Launch OmniScale. You should see the **Games** page start scanning your
installed launchers (Steam, GOG, Epic, Ubisoft Connect, Xbox, Battle.net,
EA) automatically — no configuration needed for the standard install
locations. Point it at a custom folder from the toolbar if you keep games
somewhere OmniScale doesn't find on its own.

## Uninstalling

From **Settings → Apps** (or the Start Menu entry's uninstaller), choose
**Uninstall**. OmniScale asks you to confirm before removing anything.

Uninstalling removes OmniScale's local app data — settings, library
database, downloaded runtime files — along with the program itself. This
is deliberate, not a bug: an uninstall is a genuine "remove everything"
action. If you might reinstall later, don't uninstall — just leave it, or
back up your app data folder first.

## Troubleshooting

**SmartScreen won't let me run the installer.** See "About the SmartScreen
warning" above — click **More info → Run anyway**.

**A swap didn't work, or a game won't launch after one.** Open the game in
OmniScale and press **Reset** to restore the original file. If that
doesn't help, check the log — its location is shown in the app's About
screen — and include it if you report the issue.

**I updated and my library looks empty.** This should not happen — see
["What happens when I update OmniScale?"](FAQ.md#what-happens-when-i-update-omniscale).
If it does, please [open an issue](https://github.com/TheOmniGrid/OmniScale/issues/new/choose) immediately
with your log file; this is treated as a critical bug, not a minor one.

**Still stuck?** [Open an issue](https://github.com/TheOmniGrid/OmniScale/issues/new/choose) with your
Windows version, OmniScale version, and what you were doing when it broke.
