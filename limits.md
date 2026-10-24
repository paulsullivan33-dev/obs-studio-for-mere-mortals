# Limits

What OBS Studio doesn't do, stated
plainly enough to plan around.

## It is not an editor

The deepest limit, and the one that
surprises people latest: OBS produces a
finished performance, not editable
material. There is no timeline, no
trimming beyond recording a better take,
no moving a sentence from minute forty
to minute four. Plan the workflow as
*OBS captures, an editor finishes* —
or, for meetings and lessons, as this
guide's recipes do: title and break
scenes tidy enough that no edit is
needed.

## One programme, one output picture

OBS composes a single Program feed. It
can send that feed to a recording, a
stream and the virtual camera at once —
but it cannot natively record each
source separately (the podcast
engineer's "ISO" tracks) or run two
different shows at once. Plugins can
add pieces of this; the core program
you install does not do it, and chapter
12's recipes are shaped accordingly.

## Somebody has to drive it

Scene switching, level watching and
starting on time are a person's job for
the duration of anything live. Hotkeys
and obs-websocket (chapter 10) can put
that person's controls somewhere
convenient, and the wizard can set the
numbers — but there is no autopilot,
and an unattended stream is an
unmonitored one.

## It depends on hardware it does not control

Recording quality is bounded by your
encoder, and the hardware encoders are
bounded by graphics drivers written by
NVIDIA, Intel, AMD and Apple. A driver
update can change what worked last
month; "encoding overloaded" is often a
hardware conversation, not an OBS fault.
Likewise displays and cameras arrive
through the operating system: on Linux
under Wayland, screen capture goes
through the system's sharing portal and
global hotkeys are restricted — the
platform's rules, which OBS obeys
rather than chooses.

## The edges differ by platform

Game Capture is Windows-only. The
virtual camera on Linux needs a kernel
module the program cannot install for
itself (chapter 9). Browser sources and
plugins vary in availability and polish
between operating systems, because most
plugins are volunteers' spare time aimed
first at the platform they use.

## No service behind it

There is no account, no cloud, no
support desk and no SLA — and also no
subscription, no upload you did not ask
for, and no feature removed by a
pricing change. Help is documentation,
forums and a community of people who
had your problem before you. For a
commercial event with a contract riding
on it, that trade is a decision to make
with your eyes open, and chapter 13's
paid rows exist for exactly that case.

## Streaming is bounded by your connection

No setting in OBS creates upload
bandwidth. A stream at a given
resolution, frame rate and bitrate
either fits your connection or drops
frames, and chapter 8's discipline —
wizard first, private test, local
recording alongside — is how you find
out which, before an audience does.
