# Midi2TromboneChamp
Create charts for Trombone Champ from midis, to be used with TrombLoader

## Usage
Channel 1 is used for actual notes, while Channel 2 is used for multiple slide notes.
A sequence of Channel 2 notes must end with a Channel 1 note. Also, please quantize your charts, the game hates unquantized notes.

It's strongly advised to make your own MIDI files. Trying to import ones directly from the internet will probably result in a crash or a bunch of bad notes in your chart.

## How It Works
Midi2TromboneChamp exports JSON in the following format that represents a chart:
[note position, note length, start pitch, pitch delta, pitch end]
