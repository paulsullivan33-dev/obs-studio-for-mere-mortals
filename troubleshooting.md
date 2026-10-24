# Troubleshooting

## First move, always: the Stats panel and the log

OBS tells on itself, in two places.
**View → Stats** shows the live health of
the machine: frames the renderer missed,
frames the encoder skipped, frames the
network dropped — three different
failures with three different owners, and
the panel names which one you have.
And every session writes a **log file**:
**Help → Log Files → Show Log Files**
opens the folder; the newest is the
session you just had. When a forum post
begins "it just doesn't work", the first
reply asks for the log, every time. Start
there.

## A capture is black, frozen or missing

**Symptoms:** a Display or Window Capture
shows black, or a still frame, while the
application itself is visibly fine.

**Causes, by system:**

- **macOS:** the Screen Recording
  permission was never granted (chapter
  3). System Settings → Privacy &
  Security → Screen Recording, enable
  OBS, restart it.
- **Windows laptops with two graphics
  chips:** the display is drawn by one
  chip and OBS is running on the other.
  Windows Settings → System → Display →
  Graphics: add OBS and set it to the
  chip that draws the screen (for most
  laptops, "Power saving" — try it before
  "High performance", counter-intuitive
  as that reads).
- **Linux on Wayland:** capture goes
  through the system's screen-sharing
  dialog each time. If you cancelled the
  dialog, you authorised nothing; delete
  and re-add the source and choose the
  screen in the dialog that appears.

## "Encoding overloaded"

**Symptoms:** the warning appears in the
status bar; the recording stutters or
the Stats panel's *skipped frames* climb.

**Cause:** the encoder cannot finish
each frame in the time it has. It is a
budget problem, not a bug.

**Fix, in order:** switch to a hardware
encoder if you are on x264 (chapter 2);
lower the *output* resolution (Settings →
Video) — halving the pixels quarters the
work; drop 60 fps to 30 for material
that does not need it; close the game or
the browser full of tabs sharing the
graphics chip. What not to do: raise the
quality setting, which spends the same
budget harder.

## The stream drops frames, the recording doesn't

**Symptoms:** Stats shows *dropped*
frames (network) while skipped frames
stay at zero; viewers report buffering.

**Cause:** the connection, full stop —
the encoder produced the frames and the
upload could not carry them. Chapter 8's
arithmetic is being enforced by reality.

**Fix:** lower the stream bitrate in
Settings → Output, or the resolution, and
re-test. If it drops even at modest
bitrates on a wired connection, test
without Wi-Fi (a cable is the cheapest
streaming upgrade there is) and check
nobody else is uploading a cloud backup
through the same connection.

## Nobody can hear you / the recording is silent

**Symptoms:** meters flat on the mic
channel, or a recording with picture and
no sound.

**Fix, in the order you will find it:**
is the microphone the one **named** in
Settings → Audio (not an OS "Default"
that changed when you plugged something
in)? Is the channel muted in the mixer
(the speaker icon, not the slider)? If
you record in Advanced mode, is the
source assigned to a track the recording
actually keeps? And if *you* could hear
yourself fine in headphones — monitoring
is not output; chapter 6's distinction
has caught everyone once.

## The voice echoes

**Cause, almost always:** chapter 6's
trap — a source set to **Monitor and
Output** that the recording also captures
directly (commonly the microphone, heard
once through monitoring and again through
Desktop Audio), or speakers feeding the
microphone.

**Fix:** headphones for monitoring;
Advanced Audio Properties open; find the
source arriving by two roads and close
one.

## Faces and voices drift apart

**Symptoms:** lips and words a beat
apart, on the recording but not in the
room.

**Cause:** a capture device delivering
late pictures, or Bluetooth headphones
adding their own delay to what you
monitored by (the recording may be fine
and only your monitoring lied —
check the file, not your memory of the
session).

**Fix:** chapter 6's hand-clap test and
Sync Offset on the audio channel. Small
offsets are a setting; growing offsets
across a long recording suggest a device
or driver struggling, and shortening the
test to a fresh session tells you which.

## The recording is corrupt after a crash

**Cause:** a plain MP4, interrupted
(chapter 7's whole argument). **Fix:**
there isn't one for that file; the
prevention is MKV plus remux, or Hybrid
MP4 where offered, and it takes one
minute to set up *before* the next
unrepeatable event.

## Your stream key appeared on your stream

**Fix, now, in this order:** end the
stream; reset the key on the service's
dashboard (the old one dies immediately);
put the new key into OBS. Then find the
scene that showed it and fix the scene —
usually a Display Capture pointed at a
screen that had Settings open. Chapter 8
treats the key as a password because
this is the incident that proves it.

## OBS will not start at all

**Symptoms:** no window, or a brief flash
and nothing; from a terminal, something
like `Could not load the Qt platform
plugin "xcb"` and `could not connect to
display` (this guide's lab produced
exactly that, launching OBS on a machine
with no display attached).

**Cause:** OBS is a desktop application
with no headless mode — it needs a
display session to draw its window, even
a virtual one. Launched from an SSH
session, a cron job, or a service, it has
none.

**Fix:** start it from the desktop
session it will record in. There is no
supported way to run OBS without a
display; tools that need its output
unattended drive it through a logged-in
session or the virtual camera, not
around the window.
