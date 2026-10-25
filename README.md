# OBS Studio for Mere Mortals

Almost every meeting, lesson and small
event now happens in front of a screen,
and the person running it eventually
faces the same problem: one window has
the slides, another has the speaker, the
microphone is somewhere else again, and
whatever gets recorded — if anything
does — is whatever the meeting app felt
like keeping. **OBS Studio** is the
open-source answer the streaming world
settled on: a free program that arranges
cameras, screens, slides and sound into
scenes you prepare beforehand, then
records the result to your own disk or
sends it out live, the same either way.
This guide explains how it works, how to
set it up for a meeting, a podcast or a
lesson, and how not to fool yourself
about the parts that matter: whether the
recording exists, and whether the file
will survive the day.

The lab behind this guide ran the real
program: **OBS Studio 30.0.2**, Ubuntu's
own packaged build, installed with apt
on Ubuntu 24.04 and verified as far as a
bench with no camera, no microphone, no
graphics processor and no real display
allows — which turns out to be further
than you might expect, and nowhere near
all the way. The version and help text
came from the binary itself; the program
was started under a virtual display and
produced its real first-run configuration
tree; the guide's example scene
collection (a generic community meeting)
was written by hand as a file and loaded
by the program, which created every
source in it and switched to its first
scene; the profile and websocket
configuration were read from the files
the program generated. What the lab
could not do, it did not fake: nothing
was ever recorded and nothing was ever
streamed, because the bench had nothing
to record and nowhere to stream to. The
wizard, the recording and streaming
workflows, the filters and the virtual
camera are taught from the program's
documented behaviour and labelled as
such wherever it matters — `criteria.md`
keeps the full ledger of what was run
and what was only read.

## What this guide covers

- [**What OBS Studio is**](what-obs-studio-is.md) —
  the mental model: a television studio
  shrunk into one program, free and
  open source; what it is not (an editor,
  a meeting app, a platform)
- [**The moving parts**](the-moving-parts.md) —
  scenes and sources, the audio mixer,
  the encoder, and the configuration
  folder: the five parts, what each
  holds, and what breaks when each stops
- [**Installing OBS Studio**](installing-obs-studio.md) —
  the project's own downloads for Windows
  and macOS, the two honest Linux routes,
  and the one-command check that the
  install landed
- [**First run and the Auto-Configuration Wizard**](first-run-and-the-wizard.md) —
  the interview that sets sane first
  settings for your machine, what it does
  and doesn't decide, and the three
  defaults worth changing in your first
  hour
- [**Scenes and sources**](scenes-and-sources.md) —
  building the arrangement: the source
  types, the stacking order, and a worked
  four-scene community meeting
- [**Audio and the mixer**](audio-and-the-mixer.md) —
  the two channels everything is built
  from, reading the meters, the four
  filters nearly every voice needs, and
  the echo that monitoring can cause
- [**Recording**](recording.md) —
  the settings that decide what lands on
  disk, the MKV-versus-MP4 decision that
  protects an unrepeatable event, and the
  ten-second test that outranks them all
- [**Streaming**](streaming.md) —
  the extra leg from your desk to a
  service, ingest servers and stream keys
  — and why the key is a password, not a
  setting
- [**Filters, transitions and the virtual camera**](filters-transitions-and-virtual-camera.md) —
  polish per source, how scenes change
  into each other, and appearing as a
  "camera" inside ordinary meeting apps
- [**Profiles and scene collections**](profiles-and-scene-collections.md) —
  the settings half and the scenes half,
  why there are two bundles, sharing one
  without the other, and the built-in
  remote control
- [**Backup and moving your setup**](backup-and-moving-your-setup.md) —
  the whole desk is one folder: copying
  it, what breaks when it lands on a new
  machine, the portable desk, and
  upgrading without losing your work
- [**Recipes**](recipes.md) — a community
  meeting recorded properly, a two-host
  podcast, a lesson or tutorial, and a
  small event streamed
- [**The neighbours**](the-neighbours.md) —
  Streamlabs, XSplit, vMix, the
  browser studios, the editors and
  ffmpeg: what each one trades
- [**Limits**](limits.md) — not an
  editor, one output at a time, a desk
  that must be driven, and the
  connection streaming stands on,
  stated plainly
- [**Troubleshooting**](troubleshooting.md) —
  the black capture, the overloaded
  encoder, the silent recording, the
  dropped stream, and the program that
  will not start without a display
- [**Glossary**](glossary.md) — the terms,
  collected in one place

## What it doesn't cover

Editing the video afterwards — OBS
records and streams; it does not edit,
and chapter 13 points at the tools that
do. Account setup on each streaming
platform, and growing an audience, are
the platforms' subjects, not this
guide's. The plugin ecosystem beyond
what ships in the box, scripting OBS
with Python or Lua, broadcast hardware
(capture cards get a mention, not a
buying guide), and multi-PC broadcast
setups such as NDI are likewise pointed
at, not taught.

## How to use this guide

Read chapter 1 for the model and chapter
2 before installing anything — knowing
which part holds what turns later
confusion into a named problem. Chapter
3 installs; chapter 4, done immediately
after, lets the wizard set first settings
suited to your machine. Build your first
scenes on paper using chapter 5 before
touching the program: a meeting needs
fewer scenes than you think, and the
right four beat the clever twelve.
Chapter 11 is not the optional ending —
copy the configuration folder while your
setup is still small enough that losing
it would merely be annoying. The lab's
transcripts live in
`obs-studio-lab/transcripts/`; its notes
are `examples/lab-notes.txt`.

---

## Part of the series

This guide is one of the [For Mere Mortals](https://paulsullivan33-dev.github.io/mere-mortals/) guides: plain-language guides to the tools programmers and makers use.

Related guides:

- [ffmpeg for Mere Mortals](https://paulsullivan33-dev.github.io/ffmpeg-for-mere-mortals/)
- [Audacity for Mere Mortals](https://paulsullivan33-dev.github.io/audacity-for-mere-mortals/)
- [Whisper for Mere Mortals](https://paulsullivan33-dev.github.io/whisper-for-mere-mortals/)

## License

The writing in this guide is licensed under [CC BY 4.0](https://github.com/paulsullivan33-dev/obs-studio-for-mere-mortals/blob/main/LICENSE). Code examples and lab scripts are licensed under the [MIT License](https://github.com/paulsullivan33-dev/obs-studio-for-mere-mortals/blob/main/LICENSE-CODE).
