# Rhythm System

Section-scoped rhythm engine for Logic Pro X.

The goal is to create rhythm guitar parts that are repeatable, editable at scale, and structurally consistent, while allowing section-level rhythmic identity.

Rhythm governs motion and inevitability, not expression.

## Core Principles

- Every section owns its own rhythm base
- A rhythm base is canonical for that section
- All variations derive from the section base
- Rhythm is edited once, then propagated
- New rhythmic ideas require a new base

## Structural Hierarchy

```
Ryhthm (Summing Stack)
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

##  Rhythm Base Definition

A Rhythm Base is:
- A short looping unit (typically 2 bars)
- Grid-aligned
- Harmonically neutral
- Free of fills, throws, or transitions
- The only source of rhythmic truth for the section

Rules:
- If the rhythm changes, the base changes
- Bases never reference other sections
- Bases are designed, not performed

## Variants (A / B / C)

All variants must begin as aliases of the section base.

### Roles
- A — Primary: straight implementation
- B — Accent: velocity, muting, density
- C — Transition: controlled pushes or pull-backs

Allowed:
- Velocity changes
- Note removal/addition
- Density modulation
- Micro-displacement

Disallowed:
- New rhythmic ideas
- New meters
- Independent groove logic
