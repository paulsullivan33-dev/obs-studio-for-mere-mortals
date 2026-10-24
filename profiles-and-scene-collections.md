# Profiles and Scene Collections

Chapter 2 introduced the split that runs
all of OBS: a **profile** is your
*settings*, a **scene collection** is
your *arrangement of scenes and sources*.
This chapter is the working knowledge:
how to switch jobs, how to share one
piece without the other, and how other
programs can drive the desk.

## Two menus, two different switches

Both live at the top of the window:

- **Profile** menu — the settings bundles.
  *Podcast Recording*, *Meeting Stream*:
  same scenes could serve both, but the
  output decisions differ.
- **Scene Collection** menu — the scene
  bundles. *Community Meeting*,
  *Podcast*, *Lesson*: different desks
  entirely.

The mistake everyone makes once: building
the podcast's scenes while the meeting's
*profile* is active, then wondering why
the stream key points at the meeting's
channel. The two menus are side by side
for a reason. Name profiles and
collections for the **job**, in the same
words, in pairs — *Meeting* the
collection and *Meeting* the profile —
and switching jobs becomes switching
both, in the same breath.

New bundles are born in those menus too:
**Scene Collection → New** starts an
empty desk (and chapter 5's four scenes
fill it), **Profile → New** starts
settings from the wizard or from a copy.

## Why two bundles at all

Because the two halves change at
different rates and travel separately.
Your recording *quality* decisions change
when your machine changes; your *scenes*
change when your programme changes. And
each half is shareable without the other:
send a colleague your meeting *scenes*
(the collection) and they bring their own
settings; send your successor your
*profile* and they inherit your output
discipline on their own material.

**Scene Collection → Export** writes the
collection's JSON file wherever you say;
**Import** reads one in. **Profile →
Export/Import** does the same for the
settings folder, zipped by the program.
Chapter 11 covers the wholesale version:
the whole configuration folder as a
backup.

## Remote control: obs-websocket

Since version 28, OBS carries a built-in
remote-control protocol, **obs-websocket**:
other programs on your network can ask
OBS to switch scenes, start and stop
recording or streaming, and report what
it is doing. It is how phone remote apps,
control decks and chapter 12's more
automated setups drive the desk.

It lives under **Tools → WebSocket
Server Settings**, is **off until you
enable it**, and protects itself with a
password — the program generates one the
first time it loads (you can see and
change it in that settings screen; the
lab's fresh `global.ini` had
`AuthRequired=true` and a generated
password before the server was ever
switched on). Anything on
your network that can reach the port
(the default is 4455) and knows the
password can press your buttons; on a
network you do not control, that means
leaving it off, or on with a password
you would also use for a lock. This is
OBS's nearest thing to an API, offered
in brief here in the same spirit as
other guides in this series treat APIs:
know it exists, know where its door is,
and know that the door needs a lock.

## The files themselves

Both bundles are ordinary files in the
configuration folder — profiles as
folders of `.ini` settings files,
collections as single `.json` files —
and chapter 11 backs them up by copying.
The lab for this guide generated a fresh
configuration and built a scene
collection file by hand to check the
anatomy; what it found, key by key, is
written up in `criteria.md` and the
lab's transcripts (t03, t04). The short
version is reassuring:

- A scene collection is readable JSON:
  a `name`, a `sources` array (each
  source an object with its own `name`,
  a type `id` such as `color_source` or
  `scene`, and a `settings` object —
  a scene's settings hold its `items`,
  the sources placed in it, each with a
  position and a scale), a `scene_order`
  list, and which scene is current. The
  hand-built collection from chapter 5
  loaded in the real program: every
  source was created and OBS switched
  to its first scene.
- A profile is settings in the
  traditional `name=value` form. A brand
  new profile's `basic.ini` held almost
  nothing but its name — the program
  writes your decisions into it as you
  make them and on exit.
- `global.ini` at the top of the folder
  remembers which profile and collection
  are current — and holds the
  obs-websocket facts from the section
  above: `ServerEnabled=false`,
  `ServerPort=4455`, `AuthRequired=true`,
  and a password the program generated
  on first load.

Neither file is a black box, and that
fact is the foundation of chapter 11's
whole approach.
