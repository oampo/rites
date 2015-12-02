# Rites - Musical scales and tunings library

## Example

## API Documentation

### Scales

#### Scale

```js
new rites.scale.Scale(degrees, [tuning=new rites.tuning.EqualTemperament(12)]);
```

Representation of a generic musical scale.  Can be subclassed to produce specific scales.

*Parameters*:

* degrees - `Number[]` - Array of integer degrees
* tuning - `Tuning` - The scale's tuning.  Defaults to 12-tone ET.

```js
rites.scale.Scale.prototype.getFrequency(degree, rootFrequency, octave);
```

Get the frequency of a note in the scale.

*Parameters*:

* degree - `Number` - The note's degree.
* rootFrequency - `Number` - The root frequency of the scale.
* octave - `Number` - The octave of the note.

*Returns*:

`Number` - The frequency of the note in hz.

#### Major

```js
new rites.scale.Major();
```

Major scale.

*Extends*:

`rites.scale.Scale`

#### Major

```js
new rites.scale.Minor();
```

Representation of a generic musical tuning.  Can be subclassed to produce specific tunings.

### Tunings

#### Tuning

```js
new rites.tuning.Tuning(semitones, [octaveRatio=2]);
```

*Parameters*:

* semitones - `Number[]` - Array of semitone values for the tuning.
* octaveRatio - `Number` - Frequency ratio for notes an octave apart.

#### EqualTemperamentTuning

```js
new rites.tuning.EqualTemperament(pitchesPerOctave);
```

*Extends*:

`rites.scale.Scale`

*Parameters*:

* pitchesPerOctave - `Number` The number of notes in each octave.
