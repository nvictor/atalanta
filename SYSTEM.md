# Atalanta — Logic Guitar Pattern System
*A repeatable, MIDI-native system for verse/chorus/bridge construction inside Logic Pro.*

---

## Purpose

This system is designed to:
- Maximize **speed**
- Preserve **deterministic MIDI control**
- Enable **reuse across songs**
- Avoid phrase-engine plugins

It assumes:
- Logic Pro X
- MIDI-driven guitar instruments
- Pattern-first composition

---

## 1. Canonical Pattern Length (Foundation)

Choose **one base rhythmic unit**:

- 1 bar → riffs, tight rock parts
- 2 bars → strumming, grooves (**recommended default**)
- 4 bars → only if musically necessary

**Rule:**  
All sections must be derivable from this unit.

Example:
- Verse = 2 bars × 4
- Chorus = same 2 bars, altered
- Bridge = same grid, displaced or reduced

---

## 2. Base Pattern (Immutable Source)

Create one MIDI region:

**Name:**  
`GTR – Base – 2bar`

**Characteristics:**
- Neutral rhythm
- Conservative velocity
- No fills
- Harmonically generic (root + fifth or shell chords)

⚠️ Never edit this region directly after creation.

---

## 3. Region Aliases (Critical)

Instead of copying:
- Option + Shift + Drag to create **Aliases**

Benefits:
- Global timing fixes propagate everywhere
- Groove corrections remain phase-locked
- Structural consistency across the song

---

## 4. Structural Variants

Each section is a **controlled delta** from the base.

### Verse
**Name:** `GTR – Verse – A`

Allowed changes:
- Reduced velocity
- Fewer notes (delete only)
- Muted / palm‑muted articulations

Goal: containment and clarity.

---

### Chorus
**Name:** `GTR – Chorus – A`

Allowed changes:
- Higher velocity ceiling
- Denser subdivision (8ths → 16ths)
- Open voicings
- Optional octave doubling (separate track)

Goal: energy increase without rhythmic reinvention.

---

### Bridge
**Name:** `GTR – Bridge – A`

Allowed changes:
- Rhythmic displacement
- Register shift
- Consistent rests or syncopation

Goal: contrast via offset or reduction.

---

## 5. Rhythm / Harmony Decoupling

Use a **Summing Track Stack**:

**Parent:**  
`GTR – Rhythm Engine`

**Child tracks:**
- Same instrument
- Same MIDI FX chain
- Different chord sets or voicings

Result:
- Identical rhythm
- Independent harmony

---

## 6. Track Alternatives (Micro‑Variation)

For each section track, create:

- Alternative A → primary
- Alternative B → accent variation
- Alternative C → fill / transition

Rules:
- No new rhythmic ideas
- Only accent, omit, or delay existing notes

---

## 7. Template the System

Save as a Logic Template:

**Name:**  
`Guitar – Pattern Engine`

Include:
- Base pattern
- Alias examples
- Track stack
- MIDI FX chain
- Naming conventions

This eliminates setup time on future projects.

---

## 8. Mental Model

Do not think:
> “I’m writing a verse guitar part.”

Think:
> “I’m instantiating a known rhythmic system with new harmony.”

This preserves speed and consistency across songs.

---

## Summary

- One canonical base pattern
- Aliases instead of copies
- Verse / Chorus / Bridge = controlled deltas
- Rhythm and harmony separated
- Variation via Track Alternatives
- Everything templated

This is an **engineering system**, not a performance abstraction.
