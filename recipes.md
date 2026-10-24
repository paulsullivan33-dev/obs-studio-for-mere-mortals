# Recipes

Four complete setups. Each assumes
chapters 3–5 are done: OBS installed,
the wizard run, and the meeting's four
scenes understood. Build each as its own
**scene collection** (chapter 10) so the
setups never disturb each other.

## The community meeting, recorded

**Shape:** the chapter 5 fixture, as a
collection named *Community Meeting*.
Scenes: **Title** (colour + welcome
text), **Speaker and Slides** (slides
window, camera small in the corner),
**Slides Only** (window full-canvas),
**Break** (colour + "Back in five
minutes").

**Profile:** recording only; MKV format
(chapter 7), a recordings folder you
have chosen on purpose, the hardware
encoder if your machine has one.

**Why it works:** the audience for the
recording sees the slides large and the
speaker present — the two things a lone
camera file and a lone slide export each
lose. The running order is four clicks;
the Title and Break scenes mean the file
needs no trimming at either end.

**Before you press record:** the
ten-second test from chapter 7 (voice in
the yellow, no red), the slides window
actually the window you think it is, and
the recording folder's free space
checked. Afterwards: remux to MP4 for
sharing (chapter 7) and keep the MKV as
the master.

## The two-host podcast

**Shape:** collection *Podcast*. Scenes:
**Both Hosts** (two cameras side by side,
or one wide camera if that is what you
have), **Host One** and **Host Two**
(each camera full-canvas, for emphasis),
**Title** (programme name as text over a
colour or image background).

**Sound is the programme:** one
microphone per host, each as its own
Audio Input Capture source, each with
chapter 6's filter chain — suppression,
gain, limiter — set while that host
speaks at their natural volume. Balance
the two channels so neither host's
laughter buries the other's sentence.

**Why it works:** listeners forgive a
static picture indefinitely; they do not
forgive one host at half the other's
volume. Record in MKV, at the best
quality your disk allows; if you also
stream it live, chapter 8's local-copy
advice doubles as your master.

## The lesson or tutorial

**Shape:** collection *Lesson*. Scenes:
**Screen and Face** (the application or
slides full-canvas, camera in the
corner — the workhorse), **Screen Only**
(for dense detail — code, a spreadsheet,
a diagram the class must read), **Face
Only** (for the introduction, questions
and the goodbye — people subscribe to
people), **Starting Soon** and **Break**
(text over colour) if it is live.

**Habits that pay:** rehearse the switch
to Screen Only until it is one click —
zooming the screen itself (your
operating system's magnifier, or the
application's own zoom) reads better
than squinting viewers. Captions and
editing happen afterwards, elsewhere
(chapter 14); OBS's job is a clean,
legible capture.

## The small event, streamed

**Shape:** collection *Event Stream*.
Scenes: **Wide** (one camera on the
whole stage or room), **Speaker**
(camera closer, or a second camera if
you have one), **Title**, **Intermission**
(text + the time you will return), and
**Thank You** (credits as text — names
of speakers and helpers, spelled the way
they spell them).

**Profile:** a *separate* profile for
streaming, set by the wizard against
your venue's connection — which is not
your home connection, so run the wizard
there, on the day, or accept its earlier
verdict only as a starting guess.
Chapter 8's two habits are mandatory
here: a private test stream first, and
a local recording running alongside, so
a dropped connection is an embarrassment
in the chat rather than the loss of the
event.

**Why it works:** an event stream fails
on logistics, not artistry — keys,
cables, connections, a microphone
nobody tested. The scene list is short
on purpose; the checklist is the real
recipe.
