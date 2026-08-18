# g-test

A [Songbird](https://tivra.com) project.

| | |
|---|---|
| Tempo | 120 BPM |
| Meter | 4/4 |
| Tracks | 10 |
| Clips | 4 |
| Plugins | 17 |
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

## Layout

- `g-test.bird` — arrangement & musical intent, human-readable.
- `entities/` — content keyed by stable id (clips, plugins, automation, channels). Each file stays whole until it grows large, then transparently shards into `entities/<type>/NN.json` so merges stay size-independent.
- `views/` — projections that place entities (arrangement rows, mixer bus). New views (palette, session) are added here without touching content.
- `state/` — global project state (transport, settings, sections, …).
- `samples/` & `visuals/` — media payloads, stored in R2 (see `manifest.json`).
