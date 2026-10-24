# First Run and the Auto-Configuration Wizard

The first time OBS opens, it offers to
interview you. The **Auto-Configuration
Wizard** asks what the program is for,
looks at your machine and — for streaming —
at your connection, and sets a sensible
first configuration. Old hands skip it
out of habit; for a first install it is
the fastest route to settings that are
known to suit your hardware, and you can
re-run it any time from the **Tools**
menu when the hardware or the job
changes.

## What the wizard asks

Three things, in order:

1. **What comes first:** streaming,
   recording, or the virtual camera.
   This is a priority, not a life choice
   — OBS does all three regardless — but
   it decides which numbers the wizard
   optimises. The community-meeting
   setup in this guide answers
   *recording*; an event streamer answers
   *streaming*.
2. **The video shape:** a base
   (canvas) resolution and a frame rate.
   It proposes your screen's size and
   60 or 30 frames per second. Accept
   the proposal unless you know your
   material is gentler — slides and a
   talking head do not need 60, and
   asking for it anyway costs your
   machine real work on every frame.
3. **For streamers, the service:** which
   one, and your stream key (chapter 8's
   warnings apply while it is on your
   screen). The wizard then runs actual
   bandwidth tests to the service —
   this takes a minute and looks like
   nothing is happening; it is the most
   valuable minute in the setup.

For recording, the equivalent tests are
of your machine: it benchmarks the
encoders it can find and picks the best
it is confident in — a hardware encoder
if your graphics provides one, x264 at a
sane setting if not.

## What it sets — and what it doesn't

The wizard writes its answers into your
first **profile** (chapter 10): encoder,
bitrate or recording quality, canvas and
output resolutions, frame rate. It does
**not** build scenes, choose your
microphone, or set your recording
folder: chapters 5, 6 and 7 still have
their work to do. Think of the wizard as
setting the machinery under the desk;
the desk itself is yours.

**Check:** after the wizard, open
**Settings → Output** and **Settings →
Video**. The encoder named there should
be one your machine actually has (a
hardware name if you have the graphics
for it), and the canvas should match
your screen. If the wizard could not run
— an offline machine, a skipped
interview — those two screens are where
you set the same answers by hand, and
nothing else in this guide changes.

## The defaults worth changing immediately

Whichever route you took, three chapter
7 decisions belong to your first hour,
not your first disaster:

- The **recording folder**, chosen on
  purpose (Settings → Output).
- The **recording format: MKV** (Settings
  → Output), so a crash cannot take a
  recording with it.
- Your **microphone, named explicitly**
  (Settings → Audio), not left on
  "Default" for the operating system to
  re-decide on a day you are recording.
