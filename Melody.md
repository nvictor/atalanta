# Melody System

Section-scoped melody engine for Logic Pro X.

The goal is to create melodies that are disciplined, repeatable, and emotionally precise using pitch hierarchy, terraced motion, and cell-based construction.

Melody governs meaning and narrative direction.

## Core Principles

- Every section owns its own melody base
- A melody base defines pitch reality, not performance
- All melodic variants derive from the section base
- Energy comes from rhythm and repetition, not range
- New pitch logic requires a new base

## Structural Hierarchy

```
Melody (Summing Stack)
├── Intro (Track)
│   ├── Intro – Base (Region)
│   ├── Intro – A
│   ├── Intro – B
│   └── Intro – C
├── Verse
│   ├── Verse – Base
│   ├── Verse – A
│   ├── Verse – B
│   └── Verse – C
├── Chorus
│   ├── Chorus – Base
│   ├── Chorus – A
│   ├── Chorus – B
│   └── Chorus – C
├── Bridge
│   ├── Bridge – Base
│   ├── Bridge – A
│   ├── Bridge – B
│   └── Bridge – C
├── Solo
│   ├── Solo – Base
│   ├── Solo – A
│   ├── Solo – B
│   └── Solo – C
└── Outro
    ├── Outro – Base
    ├── Outro – A
    ├── Outro – B
    └── Outro – C
```

## Melody Base Definition

A Melody base is a pitch lattice, not a finished line.

It defines:
- Allowed pitch set (≤6 tones)
- Anchor tones (1 / ♭3 / 5)
- Connective tones (2 / 4 / ♭7)
- Phrase start/end anchors
- Rhythmic grid ceiling

Rules:
- Phrase boundaries resolve only to anchors
- Connective tones never end phrases
- No chromatic pitches
- Leaps > a third must resolve immediately

## Variants (A / B / C)

All variants must begin as aliases of the section base.

### Roles
- A — Primary: narrative line using Hold → Step → Hold
- B — Density: same cells, increased rhythmic subdivision
- C — Turn: anchor swaps, octave shifts, or brief compression

Allowed:
- Rhythmic density changes
- Cell repetition
- Octave displacement
- Ending anchor substitution (1 ↔ 5)

Disallowed:
- New pitch classes
- New contour shapes
- Ornamentation or chromaticism

## Sections

Intro:
- Slowest grid
- Re-inforces tonic
- Static or rhythmic
- Resolutions to 1

Verse:
- Slower grid
- Longer holds
- Descending or static bias
- Resolutions to 5 (avoid 1 if possible)

Chorus:
- Faster grid
- Short repeating cells
- Energy via rhythm rather than pitch
- Conservative pitch set

Bridge:
- Contrast verse
- Shift to ♭3 and ♭7 for suspended tension
- Delayed resolution
- Cells shrink, syncopation, rests

Solo:
- Comments on verse; longer "verses"
- Terraced motion
- Intensity comes from rhythmic bursts

Outro:
- Loop a fragment (intro or verse)
- Slower grid
- Energy dissipates
