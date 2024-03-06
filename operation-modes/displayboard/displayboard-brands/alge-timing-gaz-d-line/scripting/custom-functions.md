# Custom Functions

| Method           | Parameters    | Description                                                                                                                                                                                                    |
| ---------------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `gaz.FormatTime` | `"precision"` | <p>Formats the converted timespan to a given precision and makes sure that the format matche the ALGE-Timing protocol<br>Example: <code>{{ "[RuntimeDisplayboard]" | gaz.FormatTime "Hundredths" }}</code></p> |

`precision` can be any of the following enumeration:

* `"Seconds"` or `0`
* `"Tenths"` or `1`
* `"Hundredths"` or `2`
* `"Thousands"` or `3`
