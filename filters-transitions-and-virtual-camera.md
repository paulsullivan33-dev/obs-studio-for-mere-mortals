# Filters, Transitions and the Virtual Camera

Three smaller instruments share this
chapter. **Filters** change a source
before anyone sees it; **transitions**
change how one scene becomes the next;
the **virtual camera** changes where the
finished picture goes. Each is a
five-minute learn with an outsized
effect on how deliberate your output
looks.

## Filters on a picture

Select a source, click **Filters** (under
the preview, or right-click the source).
Two lists live there: **Effect Filters**
change the picture itself, **Audio
Filters** are chapter 6's list, reached
from the video side. The effect filters
worth meeting first:

| Filter | What it does | Typical job |
|---|---|---|
| **Crop/Pad** | Trims the edges of a source | Removing a window's borders; tightening a camera shot — the same crop as Alt-drag, kept as a setting |
| **Colour Correction** | Brightness, contrast, saturation, hue | Waking up a dull webcam; calming an over-bright one |
| **Chroma Key** | Makes one colour transparent | The green-screen effect; your background vanishes, a scene shows through |
| **Image Mask/Blend** | Cuts a source to a shape from an image | The rounded-corner or circular camera window |
| **Sharpen** | Adds edge crispness | A gentle touch on a soft camera — heavy use looks worse than softness |
| **Scroll** | Moves a source steadily | A rolling credits or a crawling notice |

Filters stack in list order, each seeing
the previous one's output: crop away the
green screen's edges *before* chroma
keying what's left, not after. Toggle a
filter's eye icon to see the before and
after honestly — your memory of the
unfiltered picture is flattering and
wrong.

A word on chroma key, because it is the
filter everyone tries first and blames
first: the filter is the cheap part. An
evenly lit, uncreased backdrop, lit
separately from you, is what makes the
edges clean. A badly lit screen keys
badly in every program, and chapter 15
sends you to the lighting before the
sliders.

## Transitions: how scenes change

The default transition is a short
**Fade**; **Cut** is the instant change.
The choice is a tone decision: cuts for
meetings and lessons (nobody is watching
the join), fades for ceremonies and
anything that would feel abrupt. A
**Stinger** plays a short video over the
join — the animated swoosh of sports
broadcasts — and is the only transition
that needs a file prepared beforehand.

Set the scene transition and its
duration (in milliseconds) in the
transition controls beside the preview.
**Transition Override** (right-click a
scene) lets one scene always arrive
differently — the Break scene fading in
slowly, say — whatever the global
setting says.

## The virtual camera

**Start Virtual Camera**, in the
controls at bottom right, publishes your
Program feed as a webcam named **OBS
Virtual Camera**. Any application that
can choose a camera — meeting software,
a browser call — can then use your
composed scenes as its picture: slides
and face together, title cards, the lot,
inside an ordinary call.

Platform notes, because they differ:

- **Windows and macOS:** built in;
  the virtual camera appears in other
  applications once OBS has run (macOS
  asks you to approve a system camera
  extension the first time).
- **Linux:** the virtual camera needs
  the **v4l2loopback** kernel module
  installed and loaded — a separate
  package (`v4l2loopback-dkms` on
  Ubuntu/Debian). Without it the button
  is present but has nothing to publish
  to; with it, it works like the other
  platforms.

Two behaviours surprise everyone the
first time: the virtual camera shows
what **Program** shows, so scene
switching is visible to your call exactly
as to a recording — prepare in Preview
(Studio Mode, chapter 5) if the call
should not see you browse. And the
camera carries **picture only**: your
microphone still reaches the meeting
through the meeting software's own audio
settings, not through OBS.
