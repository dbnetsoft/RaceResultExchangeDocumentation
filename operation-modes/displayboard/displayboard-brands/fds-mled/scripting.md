# Scripting

### Functions <a href="#functions" id="functions"></a>

| Method           | Parameters                                                                                         | Description                                                                                                                                                     |
| ---------------- | -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `mled.Color`     | `"ColorName"`                                                                                      | <p>This function will start a new color for the following text<br>Example: <code>{{ mled.Color "Red" }}Hello</code> produces the the text Hello in red font</p> |
| `mled.EndColor`  | <p><code>&#x3C;string></code><br><code>&#x3C;length></code><br><code>"&#x3C;alignment>"</code></p> | This function will end the latest color used and fall back to the default panel color.                                                                          |
| `mled.FillColor` | `"ColorName"`                                                                                      | <p>This function will change the background color of the board.<br>Example: <code>{{ mled.FillColor "Red" }}</code> produces an all red MLED display</p>        |

Color names can be any of the following:

* Black
* Red
* Gree
* Blue
* Yellow
* Magenta
* Cyan
* White
* Orange
* DeepPink
* LightBlue

### Examples <a href="#examples" id="examples"></a>

All examples can be seen[ here](../../../../scripting/examples.md).
