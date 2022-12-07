# File Parts

## Waves list

- There will be 16 waves (possibly configurable to N waves).
- Each wave will be made out of 16? values.
- Each value will be represented by 0-F

Thus a sound wave might look like

```hex
0000FFFF0000FFFF
```

for a sample square wave.

All zeros in a wave is a special state that denotes noise should be played instead of the sample.

## SFX

A list of what waves to play, what note to play them at, and what effect to apply to the waves. Note volume too.

Additionally, how long the SFX is, and how fast it should play.

## Pattern

Includes timing information, which instruments or waves to play. And what effects (not sfx) to apply to them. Notes. Note volume.

Additionally, pattern length.

## Effects

Vibrato
Glissando

## Song

A list of which pattern to play, and for how many beats.

Or possibly do we want to allow programatic control with GOTOs?
