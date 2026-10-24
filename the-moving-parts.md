# The Moving Parts

OBS feels complicated the first time you
open it because everything is on the desk
at once. In fact it is five things, and
every panel in the window belongs to one
of them.

## 1. Scenes and sources: the picture

A **source** is one ingredient: your
screen, a window, a webcam, a picture, a
line of text, a microphone's picture-less
cousin the audio source. A **scene** is
an arrangement of sources — what goes
where, how big, what sits on top of what.

The big picture in the middle of the
window, the **Program** feed, is the
scene you have selected, and it is what
your recording or stream receives. The
Scenes list (bottom left) and the Sources
list (next to it) are where you build.
Chapter 5 is entirely about this part.

## 2. The audio mixer: the sound

Every source that makes sound gets a
channel in the **Audio Mixer** (bottom
middle): a volume slider and a meter.
Two global channels matter most —
**Desktop Audio** (everything your
computer plays) and **Mic/Aux** (your
microphone). OBS hears your computer and
your voice as separate channels so you
can balance one against the other.
Chapter 6 is about this part.

## 3. The encoder: the machinery

Turning a live picture into a video file
or a stream, thirty or sixty times a
second, is heavy arithmetic. The
**encoder** is the part that does it, and
you have a choice of engines:

- **x264** — the software encoder; your
  main processor does the work. Always
  available, always hungry.
- **Hardware encoders** — a corner of
  your graphics chip does the work
  instead: NVENC on NVIDIA cards,
  QuickSync on Intel, VAAPI on Linux
  graphics, VideoToolbox on Apple
  machines. Much lighter on the
  processor, but only present if the
  hardware and its drivers are.

You choose the encoder in Settings, once,
and mostly forget it — until a recording
stutters, at which point chapter 15 will
send you back here.

## 4. Profiles and scene collections: the setup as data

Everything you arrange is stored in two
separate bundles, and the split causes
more confusion than everything else in
OBS combined:

- A **profile** holds your *settings*:
  recording quality and format, where
  files go, stream destination, canvas
  size, hotkeys.
- A **scene collection** holds your
  *scenes and sources*: the meeting
  layout, the podcast layout.

Switching from "record the meeting" to
"record the podcast" usually means
switching both. Chapter 10 takes the two
bundles apart and shows you the files
they are made of.

## 5. The configuration folder: where it all lives

Profiles and scene collections are not
locked inside the program. They are
ordinary files in one configuration
folder, which is why a whole OBS setup
can be backed up or carried to another
machine by copying a folder (chapter 11):

| System | Configuration folder |
|---|---|
| Windows | `%APPDATA%\obs-studio` |
| macOS | `~/Library/Application Support/obs-studio` |
| Linux | `~/.config/obs-studio` |

A **portable** copy of OBS (chapter 11)
keeps its configuration beside the
program instead, so the whole desk —
program and setup together — travels as
one folder.

## How a recording flows

Your sources feed the scene you have
selected. The scene is drawn on the
**canvas** (the picture size you set,
often your screen's size). The encoder
compresses that picture, the mixer
compresses nothing but balances the
sound alongside it, and the two are
written together — to a file on disk, to
a stream server, to the virtual camera,
or to several at once. Every "why did it
come out like that?" question in OBS is
answered somewhere along that chain.

## Check: find your configuration folder

On Linux:

```bash
ls ~/.config/obs-studio
```

Check: after OBS has run once, this
folder contains `global.ini` and a
`basic` folder holding `profiles` and
`scenes`. On Windows and macOS, open the
folder from inside OBS instead:
**File → Show Settings Folder**.
