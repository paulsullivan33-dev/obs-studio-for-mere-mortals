# Audio and the Mixer

More recordings are ruined by sound than
by pictures. A slightly soft picture is
forgivable; an echoing, whispering or
clipping voice is switched off. The
mixer is where sound is won or lost, and
it is simpler than it looks: a row of
channels, each with a meter and a volume,
all summed into what your recording
hears.

## The two channels that matter most

Under **Settings → Audio** you name your
global devices:

- **Desktop Audio** — everything the
  computer plays: the other people on a
  call, a video you show, notification
  pings and all. On a meeting recording
  this is usually the remote voices.
- **Mic/Auxiliary Audio** — your
  microphone, chosen by name. "Default"
  works until the day the computer picks
  a different default; naming the actual
  microphone is the first fix in
  chapter 15 for a reason.

Any further microphones or sound inputs
arrive as **Audio Input Capture** sources
inside scenes (chapter 5) — a second
podcast mic, for instance — each with
its own mixer channel, present only in
scenes that contain it.

## Reading the meters

Watch the meters while you speak at
normal volume. The scale is decibels,
marked on the meter itself, and the
practical reading is by colour:

- **Green, most of the time** — audible
  but quiet; listeners will reach for
  their volume control, then get blasted
  by the next loud moment.
- **Yellow on the peaks of speech** —
  where you want to live: clear headroom,
  nothing lost.
- **Red** — clipping: the loudest part
  of the waveform is being cut off flat,
  and it cannot be repaired afterwards.

Set the level by moving the microphone
closer first — an inch of distance beats
ten decibels of gain — then the slider,
then gain filters if you must. Test with
a ten-second recording at the volume you
will actually speak at, not the volume
you test at.

**Check:** record yourself reading a
paragraph aloud, once quietly and once
at full presenting volume. The quiet
pass should sit in the green-to-yellow,
the loud pass should peak in yellow and
never touch red. Chapter 7 covers where
that test file lands.

## Filters: fixing the voice you have

Right-click a mixer channel → **Filters**
opens the per-source filter list. Three
earn their keep on almost every voice:

| Filter | What it does | Watch out for |
|---|---|---|
| **Noise Suppression** | Removes steady background noise — fans, hum, room tone. The RNNoise method is the stronger of the built-in choices | Too much makes voices watery and eats word-endings; it cannot remove a barking dog, only steady noise |
| **Gain** | Raises or lowers this source alone | Raising gain raises the noise floor with it; move the mic first |
| **Limiter** | A ceiling nothing crosses | Set it last; it is the safety net under the red zone, not a volume control |

A **Compressor** — loud parts pulled
down, quiet parts effectively up — is
the fourth, for voices that wander.
Filters apply **top to bottom in the
list order**: suppression before gain,
or you amplify the noise you meant to
remove; limiter last. For a podcast the
same chain on each voice keeps the two
hosts level with each other across an
hour.

## Monitoring, and the echo trap

**Monitoring** means hearing a source in
your own headphones. It is set per
source in **Advanced Audio Properties**
(right-click the mixer): Off, Monitor
Only, or Monitor and Output.

The trap: monitoring your microphone
while Desktop Audio is also a channel
can loop your voice — once directly,
once through the desktop — into a
distinct echo on the recording. The
rules that keep you safe: monitor
through headphones, never speakers
(speakers feed the microphone), and if
a recording echoes, suspect a source
set to Monitor and Output that the
recording also hears directly.

## When sound and picture drift apart

A voice slightly *behind* the lips is
usually a camera or capture device that
delivers its picture late. The fix lives
in Advanced Audio Properties: a **Sync
Offset** on the audio channel, in
milliseconds, nudged until a hand-clap
test — clap on camera, watch the spike
on the meter — lands on the picture.
Small offsets (tens of milliseconds)
are normal with webcams and capture
cards; needing hundreds suggests
something else is wrong, and chapter 15
treats it as a symptom, not a setting.
