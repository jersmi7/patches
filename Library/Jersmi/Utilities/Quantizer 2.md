# Scale Quantizer

## Description

Quantizes incoming pitch signals to one of 56 musical note sets, from single notes and intervals through chords, pentatonic scales, modes, and chromatic. Supports up to 8 polyphonic voices. Pitch signals use 1 unit per octave.

## Controls

- Root — Selects the root note and its displayed spelling.
- Scl — Selects one of the 56 note sets listed below.
- Oct — Shifts the octave from −3 to +3.
- Bias — Adjusts note emphasis from 0–100%. Higher settings make the stronger tones larger in the note display and increase the hold when an ascending pitch crosses an octave boundary.

## Ports

- O input — Pitch signal to quantize, using 1 unit per octave.
- Scale modulation input — Modulates scale selection.
- Octave modulation input — Modulates the octave shift.
- O output — Quantized pitch signal.

## Notes

### Note display and Bias

The note display (arranged like an octave on the piano) highlights the selected scale and sounding notes. As Bias increases, the stronger tones have taller note markers: the strongest grow most, secondary tones grow less, and the remaining tones keep their original size. At zero Bias, all markers have the same height. Note lettering stays the same size.

Bias affects the display and the hold at an ascending octave boundary. It does not currently expand the pitch range assigned to stronger tones.

### Available scales

Scales appear in selector order, grouped by increasing note count (1–12 notes). Steps are semitones relative to the root.

| # | Scale | Steps |
| --- | --- | --- |
| 1 | Octave Unison | 0 |
| 2 | Minor 2nd Dyad | 0, 1 |
| 3 | Major 2nd Dyad | 0, 2 |
| 4 | Minor 3rd Dyad | 0, 3 |
| 5 | Major 3rd Dyad | 0, 4 |
| 6 | Perfect Fourth | 0, 5 |
| 7 | Tritone | 0, 6 |
| 8 | Perfect Fifth | 0, 7 |
| 9 | Minor 6th Dyad | 0, 8 |
| 10 | Major 6th Dyad | 0, 9 |
| 11 | Minor 7th Dyad | 0, 10 |
| 12 | Major 7th Dyad | 0, 11 |
| 13 | Major Triad | 0, 4, 7 |
| 14 | Minor Triad | 0, 3, 7 |
| 15 | Diminished Triad | 0, 3, 6 |
| 16 | Augmented Triad | 0, 4, 8 |
| 17 | Suspended 2nd | 0, 2, 7 |
| 18 | Suspended 4th | 0, 5, 7 |
| 19 | Dominant 7th | 0, 4, 7, 10 |
| 20 | Major 7th | 0, 4, 7, 11 |
| 21 | Minor 7th | 0, 3, 7, 10 |
| 22 | Half-Dim 7th | 0, 3, 6, 10 |
| 23 | Diminished 7th | 0, 3, 6, 9 |
| 24 | Minor-Major 7th | 0, 3, 7, 11 |
| 25 | Major Pentatonic | 0, 2, 4, 7, 9 |
| 26 | Minor Pentatonic | 0, 3, 5, 7, 10 |
| 27 | Sus Egyptian Penta | 0, 2, 5, 7, 10 |
| 28 | Minor Blues Penta | 0, 3, 5, 8, 10 |
| 29 | Maj Blues/Yo Penta | 0, 2, 5, 7, 9 |
| 30 | Ryukyu | 0, 4, 5, 7, 11 |
| 31 | Insen Pentatonic | 0, 1, 5, 7, 8 |
| 32 | Hirajoshi | 0, 2, 3, 7, 8 |
| 33 | Pelog | 0, 1, 3, 7, 8 |
| 34 | Whole Tone | 0, 2, 4, 6, 8, 10 |
| 35 | Major Blues | 0, 2, 3, 4, 7, 9 |
| 36 | Minor Blues | 0, 3, 5, 6, 7, 10 |
| 37 | Messiaen Mode 5 | 0, 1, 5, 6, 7, 11 |
| 38 | Ionian Mode | 0, 2, 4, 5, 7, 9, 11 |
| 39 | Dorian Mode | 0, 2, 3, 5, 7, 9, 10 |
| 40 | Phrygian Mode | 0, 1, 3, 5, 7, 8, 10 |
| 41 | Lydian Mode | 0, 2, 4, 6, 7, 9, 11 |
| 42 | Mixolydian Mode | 0, 2, 4, 5, 7, 9, 10 |
| 43 | Aeolian Mode | 0, 2, 3, 5, 7, 8, 10 |
| 44 | Locrian Mode | 0, 1, 3, 5, 6, 8, 10 |
| 45 | Half-Whole Dim | 0, 2, 3, 5, 6, 8, 10 |
| 46 | Spanish Phrygian | 0, 1, 4, 5, 7, 8, 10 |
| 47 | Gypsy Maj Arabic | 0, 1, 4, 5, 7, 8, 11 |
| 48 | Gypsy Minor | 0, 2, 3, 6, 7, 8, 11 |
| 49 | Harmonic Minor | 0, 2, 3, 5, 7, 8, 11 |
| 50 | Ukrainian Dorian | 0, 2, 3, 6, 7, 8, 10 |
| 51 | Octatonic | 0, 1, 3, 4, 6, 7, 9, 10 |
| 52 | Messiaen Mode 4 | 0, 1, 2, 5, 6, 7, 8, 11 |
| 53 | Messiaen Mode 6 | 0, 2, 4, 5, 6, 8, 10, 11 |
| 54 | Messiaen Mode 3 | 0, 2, 3, 4, 6, 7, 8, 10, 11 |
| 55 | Messiaen Mode 7 | 0, 1, 2, 3, 5, 6, 7, 8, 9, 11 |
| 56 | Chromatic | 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11 |

## Version History

- 2.2 — September 2026: Lyte version by Jerry Smith. 56 note sets, Bias control, and note emphasis display.
- 2.1 — 24 February 2024: Jerry Smith and Rudiger Meyer.
- 2.0 — 2023: Jerry Smith and Rudiger Meyer.
- 1.0 — 2022: Jerry Smith.
