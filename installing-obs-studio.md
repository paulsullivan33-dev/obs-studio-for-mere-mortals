# Installing OBS Studio

OBS Studio is a desktop application, and
installing it is an ordinary application's
install on all three systems — no server,
no database, nothing else to stand up
first. What differs between systems is
where you get it, and the differences
matter: get it from the project or your
system's own store, not from a search
result's lookalike download site.

## Windows

Download the installer from the project's
site, **obsproject.com**, and run it. It
installs for your user account and adds
itself to the Start menu. The site also
offers a .zip of the same build — that is
the raw material of the portable setup in
chapter 11 — and a Microsoft Store
edition. All three are the same program;
the installer's release is the one this
guide's descriptions follow.

## macOS

The same site offers one download for
Apple silicon Macs and one for Intel
Macs; pick the one your machine is
(System Settings → General → About says).
Open the .dmg and drag OBS to
Applications. The first launch asks the
usual questions — and, over the following
days, the permissions that actually
matter on a Mac: **microphone**,
**camera**, and **screen recording**.
Grant them in System Settings → Privacy
& Security when asked; chapter 15's most
common Mac symptom — a black or frozen
screen capture — is usually a permission
that was never granted, not a fault.

## Linux

Two honest routes, and they are *not*
the same version:

- **Your distribution's package.** On
  Ubuntu and Debian: `sudo apt install
  obs-studio`. One command, updates arrive
  with the system's, and it is the build
  this guide's lab installed and verified
  against (see `criteria.md` for the
  version your distribution currently
  ships — distributions lag the project,
  sometimes by a version or two).
- **The project's own builds.** The OBS
  Project publishes an official Flatpak
  (on Flathub) and, for Ubuntu, a PPA.
  These track the current release. The
  Flatpak's sandbox also changes where
  configuration lives — its config folder
  sits under `~/.var/app/com.obsproject.Studio/`
  rather than `~/.config/obs-studio` —
  and can fence off some plugins and the
  virtual camera's kernel module. Nothing
  fatal; know it before chapter 10 sends
  you looking for files.

Whichever route: on Linux the virtual
camera additionally needs the
**v4l2loopback** kernel module (chapter
9); your distribution's `v4l2loopback-dkms`
package provides it, and OBS cannot
install it for you.

## Check: the program answers

However you installed it, the program
itself can confirm the install from a
terminal — the same check this guide's
lab ran first:

```bash
obs --version
```

Check: it prints a version line — the
lab's Ubuntu build answered
`OBS Studio - 30.0.2.1-3build1`, the
program's own rendering of its package
version, 30.0.2. If the
shell answers "command not found" on
Linux, the package did not land; on
Windows and macOS, simply launch the
application — the version is under
**Help → About**. Then let chapter 4's
wizard interview you before you build
anything.
