# Recording

Recording is the half of OBS with no
audience and every second chance — and
still the half where the expensive
mistakes live, because a recording
failure is usually discovered afterwards.
This chapter is the settings that decide
what lands on disk, and the habits that
make sure something does.

## Where recordings are decided

**Settings → Output** has two modes.
**Simple** mode, the default, asks plain
questions and is enough for almost
everyone:

- **Recording Path** — the folder files
  land in. Choose it on purpose; the
  default is a system video folder you
  may never otherwise open, and "where
  did it go?" is the most common first
  question in OBS's history.
- **Recording Quality** — a menu from
  "same as stream" up to **Indistinguishable
  Quality, Large File Size** and
  **Lossless** (which means what it says
  and eats disk accordingly; leave it
  alone unless you know why you are
  there). "High Quality, Medium File
  Size" is the honest default for
  meetings and lessons.
- **Recording Format** — see below; this
  is the one to get right.
- **Encoder** — chapter 2's choice. On a
  machine with a hardware encoder, use
  it for recording and save the processor
  for everything else.

**Advanced** mode replaces the plain
questions with the full machinery —
separate stream and recording encoders,
audio track selection (up to six tracks
in one file, for editors who want the
microphone and the desktop on separate
tracks), replay buffer, and per-field
numbers for everything. Nothing in this
guide needs it; knowing it exists, and
that Simple is not a toy version, is
enough.

## The format decision: record MKV

OBS offers several recording formats.
The one that matters:

| Format | Survives a crash? | Plays everywhere? |
|---|---|---|
| **MKV** | Yes — the file is whole up to the last whole second | Mostly; some editors and platforms want MP4 |
| **MP4** | A plain MP4 can be **unplayable** if OBS or the machine dies mid-recording | Yes, universally |
| **Hybrid MP4** (recent versions) | Designed to survive, like MKV | Yes |
| **FLV, MOV, MPEG-TS** | Various | Niche uses each |

The reasoning is one sentence: a
recording you cannot re-shoot — the
meeting, the event — should be written
in the format that a power cut cannot
take with it. So: **record in MKV, then
remux.** **File → Remux Recordings**
turns the MKV into an MP4 in seconds,
without re-encoding (nothing is
recompressed; the picture is identical),
and a setting in **Settings → Advanced**
can remux automatically after each
recording. Recent OBS versions add
Hybrid MP4, which aims to give you both
properties in one file; where it is
offered it is a reasonable choice, and
the MKV habit remains the one that
cannot lose.

## Starting, stopping and knowing

**Start Recording** and **Stop Recording**
sit in the controls at bottom right, and
both deserve hotkeys (Settings →
Hotkeys) — Start/Stop Recording and,
separately, **Pause** for recordings.
Three ways of *knowing* it is working,
because the button alone has fooled
everyone once:

- The recording timer and the red
  indicator in the status bar at the
  bottom of the window.
- The **CPU and disk** readouts beside
  it — a recording folder on a nearly
  full disk ends the recording for you,
  silently, at the worst moment.
- **View → Stats** for the full panel:
  frames rendered, frames dropped, and
  recording state.

Then, the habit that outranks all
settings: **the ten-second test.** Before
anything real, record ten seconds of
what you are about to do — voice, slides,
the switch to the other scene — stop,
and play the file. Every chapter 15
recording disaster (wrong window, muted
mic, camera covering the words, file in
a folder nobody checked) announces
itself in a ten-second test and hides
perfectly in a settings screenshot.

## What this guide's lab could and couldn't prove

The lab machine had no camera, no
microphone and no screen worth the name,
so no recording in this guide was
actually made and no settings screen was
opened: the settings above are the
program's own documented ones for the
build the lab installed, and the format
advice is the OBS project's standing
advice to its own users. `criteria.md`
keeps the ledger, as always.
