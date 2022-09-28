# Midi2TromboneChamp
Create charts for Trombone Champ from midis, to be used with [TrombLoader](https://github.com/NyxTheShield/TrombLoader)

## Important Notes
* Midi Channel 1 is used for actual notes, while Channel 2 is used for multiple slide notes.
* A sequence of Channel 2 notes must end with a Channel 1 note. Also, please quantize your charts, the game hates unquantized notes.
* It's strongly advised to make your own MIDI files. Trying to import ones directly from the internet will probably result in a crash or a bunch of bad notes in your chart.

## Usage
1. When you run the executable, you'll first be prompted to load your MIDI file.
2. You'll then see a prompt to enter the BPM for your track:

![BPM UI](https://i.imgur.com/kMV70la.png)

3. Next, you'll see the full prompt for your track details:

![Track Info UI](https://i.imgur.com/jn3s2a7.png)

4. After you complete that, you'll be prompted to export your finished chart. This is the song.tmb file (use that filename as-is) that you will place in your custom chart folder.
5. To use your .tmb file for a custom chart, create a new folder in the CustomSongs directory created by the [TrombLoader](https://github.com/NyxTheShield/TrombLoader) plugin using the following structure:

```
[your-song-name] # this is your folder that contains your custom chart materials
│   bg.png # your background image for the song
│   song.tmb # your .tmb file generated by Midi2TromboneChamp
│   song.ogg # your .ogg music file that will play during your song
```

## How It Works
Midi2TromboneChamp exports JSON in the following format that represents a chart:

```
[note position, note length, start pitch, pitch delta, pitch end]
```