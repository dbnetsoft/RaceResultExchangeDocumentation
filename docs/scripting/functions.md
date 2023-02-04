# Functions

## Built-in functions

A lot of basic functions are provided out-of-the-box by Scriban. You can find more information on these built-in Scriban functions [here](https://github.com/scriban/scriban/blob/master/doc/builtins.md).

## Custom functions

In addition to that, and also to interact nicely with the needs of timekeepers, RaceResultExchange also comes with a wide range of utility functions:

| Method      | Parameters | Description                          |
| ----------- | -----------| ------------------------------------ |
| `FormatRaceResult`| `<timespan>`<br />`"<format>`" | Converts a given timespan or datetime and formats it using RaceResult12 formating syntax. <br />Example: `{{ Runtime | FormatRaceResult "Hh:mm:ss,k" }}` produces `2:55:87,7`.  |
| `TrimPad`| `<string> <length>`<br />`"<alignment>"` | Trims the or pads the given string to always be as long as length and aligns it by the alignment values ("Left", "Right", "Center") Example: `{{ "Hallo, this text is too long" | TrimPad 8 "Center" }}` produces `Hallo, t`. |
| `ToTimeSpan` | `<object>` | Converts any object to a timespan, e.g. number of seconds provided by raceresult |
| `RemoveAccents` | `<string>` | Removes all accents on the given string<br />Example: `{{ "Tobìas Däuber" | RemoveAccents }}` produces `Tobias Dauber` |

## Specific functions

There are also functions available to special needs of [FDS displays](../displayboards/fdsmled/scripting.md) or [ALGE D-Lines](../displayboards/algegazdline/scripting.md).