# Glossary

**Auto-Configuration Wizard** — the
built-in setup interview (Tools menu,
and offered at first run). Tests your
machine and, for streaming, your
connection, then proposes encoder,
resolution and bitrate. Chapter 4.

**Bitrate** — how much data per second
the encoder may spend, in kilobits or
megabits per second. More bits, finer
picture, bigger files and a harder job
for your connection. Chapters 7 and 8.

**Browser source** — a source that is a
web page, rendered inside OBS: timers,
live graphics, chat overlays. Chapter 5.

**Canvas (base) resolution** — the size
of the picture OBS composes, usually
your screen's size. Distinct from the
output resolution, which is what the
encoder actually sends or saves.
Chapter 4.

**Chroma key** — the filter that makes
one colour (classically green)
transparent, so a background shows
through where the presenter stood.
Chapter 9.

**Dropped frames** — stream frames that
never reached the service because the
connection could not carry them. A
network symptom, visible in View →
Stats. Chapter 8.

**Encoder** — the engine that compresses
live video into a file or stream: x264
(software, on the processor) or a
hardware encoder (NVENC, QuickSync,
VAAPI, VideoToolbox) on the graphics
chip. Chapter 2.

**Filter** — a per-source adjustment:
correction and effects on the picture
(crop, colour, chroma key), processing
on the sound (suppression, gain,
limiter). Applied in list order.
Chapters 6 and 9.

**Hotkey** — a key combination that
performs an OBS action: switch scene,
start or stop recording, mute. Set per
profile in Settings → Hotkeys.

**MKV / MP4** — recording file formats.
MKV survives a crash whole and is this
guide's recommended recording format;
MP4 is what players and platforms
expect, and a plain MP4 can be ruined
by the same crash. **Remuxing** converts
one to the other without re-encoding.
Chapter 7.

**Monitoring** — hearing an audio source
yourself, through headphones. Set per
source in Advanced Audio Properties;
the usual suspect when a recording
echoes. Chapter 6.

**obs-websocket** — the remote-control
protocol built into OBS since version
28: other programs — scripts, phone
apps, control decks — can switch
scenes, start and stop output, and read
state over your local network. Chapter
10.

**Portable mode** — running OBS so its
configuration lives beside the program
rather than in your user folders: the
whole setup travels as one folder.
Chapters 10 and 11.

**Profile** — the bundle of *settings*:
output quality and format, recording
folder, stream destination, canvas,
hotkeys. Stored as files in the
configuration folder. Chapter 10.

**Program / Preview** — Program is the
feed being recorded or streamed;
Preview, in Studio Mode, is the scene
you are preparing next. Chapter 5.

**RTMP** — the long-standing protocol
for pushing a live feed to a streaming
service: a server address (the RTMP
URL) plus a stream key. Chapter 8.

**Scene** — an arrangement of sources:
one complete picture (with its audio)
that you can switch to. Chapter 5.

**Scene collection** — the bundle of
*scenes and sources* for one job — the
meeting, the podcast — stored as a JSON
file in the configuration folder.
Chapter 10.

**Source** — one ingredient of a scene:
a screen, window, camera, image, text,
web page, media file or audio input.
Chapter 5.

**Stream key** — the secret string that
tells a streaming service whose channel
a feed belongs to. A password in every
way that matters. Chapter 8.

**Studio Mode** — the split view:
Preview beside Program, with a
Transition button between them, so you
can prepare the next scene without
showing your work. Chapter 5.

**Transition** — how one scene becomes
the next on Program: a cut, a fade, or
a stinger video played over the join.
Chapter 9.

**Virtual camera** — OBS's Program feed
published as a webcam named "OBS Virtual
Camera", for meeting software to use as
its picture. Chapter 9.
