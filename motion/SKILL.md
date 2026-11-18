---
name: motion
description: Make animations and motion graphics that look directed rather than generated: product promos, launch clips, social reels, animated explainers, UI demos rebuilt from screenshots, logo stings, character shorts, and interface motion on the web. Covers the concept, rhythm, timing curves, camera, transitions, character acting, sound, and how to check your own frames before a human watches. Tool-agnostic (Remotion, CSS/Web Animations, Motion, GSAP, Lottie, Manim, canvas, Blender scripts). Use whenever asked to animate something, make a video or reel, or review why an animation feels cheap.
---

# Motion that looks directed

Most generated animation fails the same way: things fade in, sit there, fade out, and the next thing
fades in. Every move uses the same soft ease, nothing causes anything, and there is no stillness, so
nothing lands. The viewer reads it as a slideshow or a screensaver within a second.

This skill is the craft that avoids that. The numbers below are starting points that have worked
in practice; if you can see a better choice for the piece in front of you, make it and say why. The
checks at the end matter more than any single rule.

## Before building: decide what the picture is

1. **The one thing.** Write the single idea a stranger should be able to repeat after one watch.
   If there are three things, there are three films; pick one.
2. **Where it plays.** Landscape site hero, vertical reel (phone, muted, ~1 s to hook, UI overlays
   on the edges), in-app UI, a loop. This sets size, length, text size and the first frame.
3. **Real material.** Use the product's real UI, strings, colours, fonts, logos and numbers. Rebuild
   UI from screenshots rather than inventing it. Ask for what you can't find; never make up claims.
4. **Three concepts** that differ in *structure*, each one sentence about the picture (not the
   product): one element transforming through everything, one continuous move through scale, a
   chain reaction, a real situation acted out, a before/after through a lens, a physical metaphor.
   For each: the first frame, what carries each transition, what it rules out. Let the human pick
   when there is one; otherwise pick and say why.
   Prefer **real situations people recognise** over clever analogies. If the viewer has to decode
   a metaphor, most of them leave before they do.
5. **Beat sheet.** A table: time · beat · what moves · what is still · what carries into the next
   beat · what the viewer understands (the *read*) · sound. Write the reads first and let them set
   the length.

## The three rules

1. **Carry every boundary.** Between two beats, something on screen survives and *becomes* the next
   beat: a tapped button grows into the sheet it opens, a line becomes the grid of the next scene,
   the camera pushes into a card until its inside is the new stage. If you'd describe a boundary as
   "then we see…", it's a replacement; rewrite it as "the X becomes…". Keep the element's identity
   (same id, same node) through the change; a cross-fade between two elements is a cut in disguise.
2. **Every reaction has a cause.** UI that animates on its own reads as a screensaver. A finger, a
   pointer, a falling object, a character's hand: something visible makes each change happen.
3. **The idea is in the picture.** If the point needs a caption to land, change the picture.

Useful carries: container morph (position, size and corner radius into another rect) · push-through
(zoom into a small thing until its inside fills the frame) · circular reveal from the subject · hop
on an arc with a landing squash · many items gathering into one · a shape collapsing into a line
that belongs to the next scene · one continuous world the camera travels across. Hard cuts belong
inside a burst of quick hits or into the end card.

## Rhythm and reads

- **Uneven on purpose.** Vary beat lengths a lot (a 4× spread between shortest and longest is a good
  floor). Equal beats make a metronome.
- **Stillness is what makes moves land.** Aim for roughly a quarter of the running time truly still,
  picture and sound, including at least one rest of a second or more, often just before the climax.
  A "hold" with a slow drift in it is not a hold.
- **Pack hits into bursts** (several big changes in about a second) instead of spreading them evenly.
- **One meaning at a time.** Fast actions, slow meanings: a tap can take 0.2 s, but "that opened the
  settings" needs about a second to sink in. Never stack two new meanings.
- **Text must stay readable**: roughly letters ÷ 15 + 1.5 s for a line, less for a one-word label.
  Words meant only as rhythm hits can flash; say so in the beat sheet.
- **Vary the exits.** Don't end consecutive beats the same way.
- **The first second is the hook**, especially on social: already moving, legible and specific. No
  fade-up from black, no logo first.

## Timing curves

One soft ease on everything makes the film mushy. Choose per move:

- **Arrivals snap, then settle**: most of the distance early (an expo/quint-out, or a spring). This
  is the "launch clip" feel.
- **Travel between two rests** can be symmetric (ease-in-out).
- **Exits** gather slowly and leave fast (ease-in), and are shorter than entrances.
- **Springs** for anything physical or UI-native: frequency ~1.5–4 Hz, damping ratio 0.5 (bouncy,
  for pops and badges) to ~0.95 (heavy panels, no bounce). Pass velocity along: a thing that arrives
  fast should carry that speed into its next motion.
- **Text and blocks land** with position + scale, with opacity finishing early. Opacity-only
  entrances look like presentation software.
- **Contact**: a press dips and rings out; an impact squashes along the direction of travel and
  recovers. Small squash-and-stretch on fast objects sells weight; overshoot on *everything* reads
  as cheap.

## Camera

Treat the frame as one virtual camera over a world, not a sequence of layouts.

- **Lead the subject.** Frame where it will be a beat later; for a fast move, key the camera at the
  landing spot so it arrives first. A camera that chases always lags.
- **Then go dead still.** Hold frames should be identical, not drifting.
- **Zoom in log space** so a 1→4× push feels as even as 4→16×. For very deep zooms, key where an
  anchor point sits *on screen* plus the zoom, not world positions.
- **Give moves a reference.** On a flat or dark background, camera motion is invisible; a faint dot
  grid or parallax layers make it readable.
- Small handheld drift (a few px, two slow incommensurate wobbles) adds life between holds; jolts
  belong to impacts, not decoration.

## Look

One ground covering most of the frame, one ink, and **one** accent colour with **one** meaning (the
cause, or the result). Big quiet grounds, small elements on them. Start from the product's own theme
when there is one. Display type tight and confident; body in a clean grotesk; mono for times and
micro-labels.

Leave out the stock motion-graphics tells: particles, confetti, sparkles, lens flares, neon glow,
RGB split, glitch, grid floors, shockwave rings, random camera shake. If a moment needs emphasis,
make the thing itself land harder.

## Characters (if the piece has any)

The bar is "doesn't look wonky" before it's "charming":
- Weight: anticipation before a move, overshoot and settle after, follow-through on loose parts
  (hair, straps, ears) that stays small and attached.
- Moving holds: breath and blinks so a still character is alive. Keep them small; if the character
  visibly shivers, cut the amplitude.
- No teleporting between poses, no floating props, no stiff single-curve limbs; hands and feet
  connect to what they touch.
- Big readable faces at the delivery size (eyes and mouths larger than feels natural for a phone
  screen), eyelines that clearly point at things.
- One physical gag the viewer can predict, escalated, then paid off. Dialogue optional, never the
  only carrier of the joke.

## Sound (if there is audio)

- A small palette of materials (air for moves, a knock for taps, a low hit for landings, a bright
  tick for confirmations) in one shared reverb, rather than a different beep for every event.
- Place sounds from the animation's own event times so retiming moves them too. Fewer sounds than
  beats.
- Rests are silent. The first sound after a silence is the loudest-feeling moment; use it.
- Social video is mostly watched muted: the picture must work alone. Master anyway (around −14 LUFS
  for reels, true peak ≤ −1 dBTP).

## Build so it can be checked

- **Every frame is a pure function of time.** No `Math.random()` without a seed, no wall clock, no
  state carried between frames. Then any frame can be rendered, compared and fixed in isolation.
- **Pre-simulate physics** at a fixed high rate once and sample by time; never integrate inside the
  render path.
- **Discrete things don't blur.** Digits, text and state changes switch at frame times; only
  geometry gets motion blur. Use real (multi-sample) motion blur for anything moving more than about
  80 px per frame at 1080p30; never fake it with a CSS blur filter.
- Keep the film's data (beats, reads, events, element ids) separate from drawing, so it can be
  retimed and checked without touching the view code.
- Renders with motion blur are slow and memory hungry: iterate on a low-resolution draft without
  blur, and render the final once the draft is accepted.

## Look at your own frames before anyone else does

You can't judge motion from code. Render and actually open the images:

1. **Contact sheet**: one frame per beat (or every 0.5 s) in a grid. Does each frame read? Is the
   one thing visible? Does the first frame hook?
2. **Frame strips** across each transition and each contact: every frame in a short window. This
   catches one-frame pops, teleports and cross-fades that a contact sheet hides.
3. **Self-check list**: every boundary carried or deliberately cut · every change has a visible
   cause · ~25% stillness with one rest ≥1 s · beat lengths uneven · no two reads overlapping ·
   all text up long enough · subjects inside the frame and the platform's safe zone · nothing faster
   than the shutter without blur · no stock effects.
4. **An independent review.** The session that built it knows what every frame was meant to say, so
   it can't see what the frames actually say. Hand the frames, the brief's one thing and the beat
   sheet (nothing else) to a fresh agent or person and ask for scores 1–10 on: hook, the one thing,
   reads, continuity, rhythm, craft, and sound on paper. Calibrate it hard: 5 is competent student
   work, 7 is good professional work, 8 is shareable. Ask for 5–10 concrete fixes with timecodes and
   numbers, at least one aimed at making it worth sharing. Apply what holds up; ignore what conflicts
   with the brief or the human's taste.
5. **Then show the human**, with what the review said and what you changed.

When the human corrects something about taste, write it down as a rule for the next piece, and let
it override the defaults here where they disagree.
