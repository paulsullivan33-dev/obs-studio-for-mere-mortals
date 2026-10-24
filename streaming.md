# Streaming

Streaming is recording with an audience
and no second chance. The picture, the
sound and the scene-switching are exactly
the ones from the previous chapters; what
changes is where the encoder's output
goes — down your internet connection to
a streaming service, which passes it on
to viewers — and what that journey asks
of you.

*Honesty note, once, for the whole
chapter: this guide's lab ran on a
machine with no camera, no microphone
and no audience, so no live stream was
sent. What follows is the documented
setup, checked against the installed
program's own settings screens and help
text; `criteria.md` keeps the ledger.*

## The three things a stream needs

Under **Settings → Stream**:

- **Service** — Twitch, YouTube, Facebook
  Live and a list of others ship in the
  menu; **Custom** covers anything else
  that speaks the same protocol.
- **Server** — the ingest address the
  service gives you, usually the
  recommended one in the list. Pick the
  geographically near one it suggests.
- **Stream key** — a long secret string
  from your account on the service. OBS
  sends it; the service files your stream
  under your channel because of it.

The protocol underneath nearly all of
this is **RTMP**: an old, plain, reliable
way of pushing a live feed to a server.
You will rarely type the letters, but
when a service says "RTMP URL and key",
those are the Server and Stream Key
boxes above.

## The stream key is a password

Treat it with exactly a password's care:

- Whoever holds your key can stream to
  your channel *as you*, until you reset
  it. There is no second factor.
- **Never let it appear on screen.** The
  classic accident is showing your own
  Settings window — key visible — on your
  own stream. OBS masks the key behind a
  Show button for this reason; leave it
  masked, and never make a scene out of
  the window that contains it.
- If it leaks, reset it on the service's
  dashboard; the old key dies at once.
  Then put the new one into OBS.

## Choosing stream settings

Resolution, frame rate and **bitrate**
(how much data per second the encoder
may spend) trade against each other, and
all three are capped by your *upload*
speed, which is the smaller number on
most home connections. Rather than guess,
run **Tools → Auto-Configuration
Wizard** (chapter 4) told that you
stream: it tests your connection to the
service and proposes numbers. Accept
its proposal for your first streams; the
judgement to override it comes from
watching your own results, in this
order:

- **Dropped frames** (the counter in
  **View → Stats**) climbing during a
  stream means the connection cannot
  carry what you are sending. That is a
  network fact, not a settings opinion:
  lower the bitrate, or the resolution,
  and it stops.
- **A soft or blocky picture in fast
  motion**, with no dropped frames, is
  the encoder wanting more bits than the
  bitrate allows: raise the bitrate if
  your upload has room, or lower the
  resolution so the bits it has go
  further.
- **Your computer struggling** (fans,
  a stuttering preview, "encoding
  overloaded" warnings) is chapter 15
  territory and usually a hardware-encoder
  conversation.

## Before anyone is watching

Two habits separate a calm first stream
from a famous one:

1. **Test with a private stream.** Every
   major service has an unlisted, private
   or test mode; Twitch additionally has
   a bandwidth-test mode that sends data
   without going live. Run your whole
   show — scenes, sound, an hour of it —
   to an audience of nobody, and watch
   the recording of it afterwards.
2. **Record locally at the same time.**
   **Settings → Output → Recording** can
   run alongside the stream. If the
   stream fails, the local file is the
   event anyway; if the stream succeeds,
   the local file is the better-quality
   copy you upload later.

And one from chapter 6 that matters
doubly live: check the microphone meter
moves *before* you start. The most
common first-stream disaster is not
technical at all — it is a perfect
picture of someone talking, in silence,
to an audience too polite to say so for
ten full minutes.
