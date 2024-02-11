# Functions

### Built-in functions <a href="#built-in-functions" id="built-in-functions"></a>

A lot of basic functions are provided out-of-the-box by Scriban. You can find more information on these built-in Scriban functions [here](https://github.com/scriban/scriban/blob/master/doc/builtins.md).

### Custom functions <a href="#custom-functions" id="custom-functions"></a>

In addition to that, and also to interact nicely with the needs of timekeepers, RaceResultExchange also comes with a wide range of utility functions:

| Method             | Parameters                                                                                         | Description                                                                                                                                                                                                                    |
| ------------------ | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `FormatRaceResult` | <p><code>&#x3C;timespan></code><br><code>"&#x3C;format>"</code></p>                                | <p>Converts a given timespan or datetime and formats it using RaceResult12 formating syntax.<br>Example: <code>{{ Runtime | FormatRaceResult "Hh:mm:ss,k" }}</code> produces <code>2:55:87,7</code>.</p>                       |
| `TrimPad`          | <p><code>&#x3C;string></code><br><code>&#x3C;length></code><br><code>"&#x3C;alignment>"</code></p> | Trims the or pads the given string to always be as long as length and aligns it by the alignment values ("Left", "Right", "Center") Example: `{{ "Hallo, this text is too long" \| TrimPad 8 "Center" }}` produces `Hallo, t`. |
| `ToTimeSpan`       | `<object>`                                                                                         | Converts any object to a timespan, e.g. number of seconds provided by raceresult                                                                                                                                               |
| `RemoveAccents`    | `<string>`                                                                                         | <p>Removes all accents on the given string<br>Example: <code>{{ "Tobìas Däuber" | RemoveAccents }}</code> produces <code>Tobias Dauber</code></p>                                                                              |

### Specific functions <a href="#specific-functions" id="specific-functions"></a>

There are also functions available to special needs of [FDS displays](https://dbnetsoft.github.io/RaceResultExchangeDocumentation/displayboards/fdsmled/scripting/) or [ALGE D-Lines](https://dbnetsoft.github.io/RaceResultExchangeDocumentation/displayboards/algegazdline/scripting/).
