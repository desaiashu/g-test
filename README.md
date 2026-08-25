# g-test

A [Songbird](https://tivra.com) project.

| | |
|---|---|
| Tempo | 120 BPM |
| Meter | 4/4 |
| Tracks | 30 |
| Clips | 21 |
| Plugins | 44 |
| Automation lanes | 0 |

## Tracks

- audio
- Chords
- Bass
- Hall
- Plate
- Delay
- Color
- MIDI
- MIDI
- Audio
- MIDI
- Audio
- Audio
- MIDI
- Audio
- MIDI
- MIDI
- Audio
- MIDI
- MIDI
- MIDI
- Audio
- Audio
- MIDI
- MIDI
- MIDI
- Audio
- Harmony
- Bass
- Melody

## Layout

- `g-test.bird` — arrangement & musical intent, human-readable.
- `entities/` — content keyed by stable id (clips, plugins, automation, channels). Each file stays whole until it grows large, then transparently shards into `entities/<type>/NN.json` so merges stay size-independent.
- `views/` — projections that place entities (arrangement rows, mixer bus). New views (palette, session) are added here without touching content.
- `state/` — global project state (transport, settings, sections, …).
- `samples/` & `visuals/` — media payloads, stored in R2 (see `manifest.json`).
