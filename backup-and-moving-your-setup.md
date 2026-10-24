# Backup and Moving Your Setup

An OBS setup is hours of small decisions —
scenes placed, levels set, filters tuned.
The good news, rare among creative
applications, is that the whole setup is
files in one folder (chapter 2), and
backing it up is copying that folder.
This chapter is the copying, done
deliberately, plus what breaks when the
folder lands on a different machine.

## What counts as "your setup"

Everything you have made lives under the
configuration folder:

| Piece | Where | Holds |
|---|---|---|
| Profiles | `basic/profiles/<name>/` | Your settings: output, stream, video, audio, hotkeys |
| Scene collections | `basic/scenes/<name>.json` | Your scenes and sources |
| The rest | `global.ini`, `plugin_config/`, logs and more | Program-wide state, plugin data |

Copy the **whole folder** and you have
the whole desk. Copy only one profile
folder or one scene-collection file and
you have that piece — which is sometimes
exactly what you want, and chapter 10
covers exporting single pieces from
inside the program.

**Check:** make the copy, then look
inside it before you trust it:

```bash
cp -r ~/.config/obs-studio ~/obs-backup-2026-10-23
ls ~/obs-backup-2026-10-23/basic/scenes
```

Check: your scene collections are listed
as `.json` files. A backup you have not
listed is a hope, not a backup. (On
Windows and macOS, copy the folder from
the table in chapter 2 the same way —
**File → Show Settings Folder** opens it.)

## Moving to a new machine

Install OBS on the new machine, run it
once so it builds its own folder, close
it, and replace the configuration folder
with your copy. Your scenes, profiles and
settings arrive intact. What then needs
repair is everything that pointed
*outside* the folder:

- **Files your sources use.** An Image
  source remembers a *path*
  (`/home/you/Pictures/title.png`); on
  the new machine that path is empty air
  until you copy the pictures too, or
  re-point the source. OBS shows a
  missing-files warning when a
  collection references files it cannot
  find — believe it, and use it as your
  checklist.
- **Devices.** The webcam named in a
  Video Capture Device source is the old
  machine's webcam. Re-select the
  device in the source's properties on
  first use; microphones (chapter 4's
  named device) likewise.
- **The stream key travels with the
  profile.** Convenient, and a reason to
  guard the backup like a password: it
  contains one (chapter 8). A setup
  backup on a shared drive is a stream
  key on a shared drive.

## The portable desk

On Windows, the .zip build (chapter 3)
offers a stronger trick: run it with a
`obs_portable_mode.txt` file beside the
executable (or the `--portable` flag)
and the program keeps its configuration
in a folder beside itself. That folder —
program *and* configuration — copied
whole to a USB stick or a second
machine, is a desk that survives your
main computer's worst day and runs
identically from the copy. It is the
strongest form of "backup" OBS offers,
at the price of updating that copy by
hand when the program updates.

One platform warning, because this
guide's lab checked: on a packaged Linux
install the `--portable` flag is accepted
but portable mode stays **off** — the
program's own log says `Portable mode:
false`, and the configuration goes to
`~/.config/obs-studio` as usual. The
portable desk is a Windows .zip-build
feature; on Linux and macOS, the
copy-the-folder backup above is the
whole of the trick.

## Upgrading OBS

Upgrades are ordinary application
updates, and OBS carries your
configuration forward — profiles and
collections from the previous version
open in the new one. The discipline is
the same as any tool you depend on:

1. **Copy the configuration folder
   first.** Five minutes, once, before
   the update you are excited about.
2. **Update plugins separately.** A new
   OBS sometimes needs new builds of
   third-party plugins; a plugin that
   fails to load reports itself in the
   log and simply absents itself from
   your scenes — another reason to open
   your main collection and look before
   the day you need it.
3. **Don't expect the reverse trip.**
   A configuration written by a newer
   OBS may not open in an older one.
   Downgrading is a restore-the-backup
   operation, not an uninstall.
