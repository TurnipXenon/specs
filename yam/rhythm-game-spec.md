# Rhythm Game Spec

## Overview

Mimic the gameplay for Theatrhythm Curtain Call: https://www.youtube.com/watch?v=HY1E5pH94bQ

This is version 2. The original version 1 exists as [RhythmGameSpecV1.md](./rhythm-game-spec-v1)

### Why do have v2?

Our initial plan to make rhythm game failed due to it being overcomplicated, and - at the same time - very fragile. I realized I was doing something Data-Oriented but has been doing a mix of Object-Oriented Design with Data-Oriented Design. So, I would end up keeping references with resources that is not data because I also wanted the data to be local with the logic that are reliant on them. The data, as I would later on learn, would need to be known by other resources that are neither children nor parent of this object's that own these data.

For our v2, we want to be strictly data-oriented. Here's our general plan:

1. Try to plan it out and not just wing it. This project seems to be more complicated than we anticipated. Additionally, we have to unlearn object-oriented design or be careful with it since Godot's API is still object-oriented.
2. Start from scratch since I don't want my design decisions to be too entangled with my initial design.

### Principles for our design

1. Layer 1 - Data: We want our game's important states to be representable as an easily serializable data.
2. Layer 2 - Logic: We want our game logic to not be part of the data, and be as game engine agnostic as possible. Our logic should not know about Godot's existence.
3. Layer 3 - View: We want Godot's job to only serve as a visualizer.

## Work

- [x] Get audio for inspo
- [x] Design data structure
- [x] Implement attaching meta of the song with the data structure
- [x] Implement playing song via Chart metadata
- [ ] Figure out dynamic timing (base it on osu)
	- Try to figure out the beat of the song maybe through a website: https://tunebat.com/Analyzer
- [ ] Figure out how to chart the song
	- [ ] How to place a beat
	- [ ] How to replay the song
	- [ ] How to place two beats at once
	- [ ] How to place a slide
	- [ ] How to place a hold
	- [ ] How to place a hold and a curve
	- [ ] How to adjust the curve
- [ ] v1 Post-mortem

## Chart Structure

Reference: https://osu.ppy.sh/wiki/en/Client/File_formats/osu_%28file_format%29

**ChartMeta**

- SongName: string
- AudioFilename: string
- TimingPoints
	- Time: integer = start of timing section
	- BeatLength: float = the duration of a beat in milliseconds
		- If BPM = 132; then BeatLength = 60 000 ms / 132 BPM = 454
		- 60 000 ms / x BPM = BeatLength
	- Meter: integer = amount of beats in a meter
- HitObjects
	- Timing: ulong = time to react to the object from the beginning of the song
	- Y: integer = location across the direction that the beats are moving
	- Type: integer enum = type of hit object, see **HitType**
	- Channel: integer = relevant to hold, tells which of the holds are connected
	- HoldCurvePriority?: boolean = if there are two hold channels active, prioritize the one with this property set as true
	- BezCurveStart: Vector<2D> = the position of the handle of the bezier curve from the start. If the beats are moving left to right, this would be the position to the right.
	- BezCurveEnd: Vector<2D> = the position of the handle of the bezier curve from the end. If the beats are moving left to right, this would be the position to the left.

_Note_:

- We might have issues with different screen resolution when it comes to the BezCurve

**HitType**

- -1 Unknown
- 0 Unmarked
- 1 Hit Circle
- 2 Slide
- 3 Hold Start
- 4 Hold Middle
- 5 Hold Release
- 6 Slide to Hold Release

## Document Changelogs

- 2024-04-26: Created
