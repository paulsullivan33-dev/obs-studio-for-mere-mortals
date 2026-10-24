# Scenes and Sources

This is the chapter the rest of the guide
stands on. A scene is an arrangement; a
source is an ingredient; the Program feed
shows the scene you have selected. Build
scenes before you need them, name them
for the moment they serve, and switching
during a recording becomes a single
click instead of a scramble.

## The source types you will actually use

| Source | What it shows | Typical job |
|---|---|---|
| **Screen / Display Capture** | A whole monitor | Demonstrations, slides shown full-screen |
| **Window Capture** | One application's window | Slides or a document, without the rest of your desktop |
| **Video Capture Device** | A webcam or camera | The speaker |
| **Image** | One picture file | A title card, a logo |
| **Image Slide Show** | A folder of pictures, in turn | A holding screen before an event |
| **Text** | Words you type, styled | Titles, names, "back in five minutes" |
| **Browser** | A web page, rendered inside OBS | A timer, a live graphic, a chat overlay |
| **Media Source** | A video or audio file, played | An intro clip, background music |
| **Audio Input Capture** | A microphone or sound input | A second mic beyond the global one |
| **Colour Source** | A flat rectangle of colour | Backgrounds behind text |

The exact names vary a little between
Windows, macOS and Linux — a screen is a
"Display Capture" in one list and a
"Screen Capture" in another — but the
jobs are the same everywhere. Game
Capture exists on Windows only; chapter
14 counts that among the limits.

Three habits make sources behave:

- **Order is stacking.** In the Sources
  list, higher covers lower. The camera
  goes *above* the slides if you want
  your face over them; below, it is
  hidden behind them.
- **The eye and the lock.** The eye icon
  hides a source without removing it;
  the padlock stops you dragging it by
  accident mid-recording. Lock anything
  you have carefully placed.
- **A scene is also a source.** You can
  place one scene inside another, so a
  camera arrangement you reuse — your
  face in the corner, say — is built
  once and dropped into every scene that
  needs it.

## A worked example: the community meeting

The fixture this guide builds, in the
lab and in the recipes: recording a
monthly community meeting — one speaker,
slides, an audience that is mostly
watching the recording afterwards. Four
scenes cover the whole evening:

| Scene | Sources, top to bottom | When it is on |
|---|---|---|
| **Title** | Text ("Community Meeting — welcome") over a Colour Source | Before the start, and at the end |
| **Speaker and Slides** | Video Capture Device (small, corner), Window Capture (the slides) | The talk itself |
| **Slides Only** | Window Capture, full canvas | When the slide is dense and the face would cover it |
| **Break** | Text ("Back in five minutes") over a Colour Source | The interval |

Build them in that order and the meeting
runs on four clicks. To add a source:
select the scene, click **+** under
Sources, choose the type, name it for
its job ("Slides", not "Window Capture
3") — the name is what future-you will
read under pressure.

**Check:** click through the four
scenes. Each switch should be instant,
each scene complete — nothing to fetch,
resize or unmute as you arrive at it.
If a scene needs fixing when you land
on it, it was not finished when you
built it.

## Sizing and placing

Drag a source to move it; drag its
corners to resize; right-click →
**Transform** for exact numbers and for
**Crop** (hold Alt and drag an edge on
Windows and Linux). Two commands earn
their place in muscle memory:

- **Fit to screen** (Ctrl+F in the
  transform menu) — a source exactly
  fills the canvas.
- **Stretch to screen** — fills it by
  distorting; almost never what you
  want for a camera.

A camera corner that looks right is
usually one quarter to one fifth of the
canvas width, with the same margin from
two edges. That is a starting point to
adjust, not a rule — check it against
your own slides, especially that it does
not cover words the audience must read.

## Preview, Program and Studio Mode

By default, selecting a scene puts it
straight on the Program feed — what is
being recorded *now*. **Studio Mode**
(Settings → General, or the button beside
the transition controls) splits the view:
**Preview** on the left, where you can
prepare the next scene, and **Program**
on the right, which the audience is
seeing; the **Transition** button moves
Preview to Program. For a rehearsed
meeting the simple mode is enough; for
anything with surprises, Studio Mode is
the difference between preparing a scene
and publishing your preparation.
