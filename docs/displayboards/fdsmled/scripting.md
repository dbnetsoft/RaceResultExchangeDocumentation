# Scripting

## Functions

| Method      | Parameters | Description                          |
| ----------- | -----------| ------------------------------------ |
| `mled.Color`| `"ColorName"` | This function will start a new color for the following text <br />Example: `{{ mled.Color "Red" }}Hello` produces the the text Hello in red font|
| `mled.EndColor`| `<string>`<br />`<length>`<br />`"<alignment>"` | This function will end the latest color used and fall back to the default panel color.|
| `mled.FillColor` | `"ColorName"` | This function will change the background color of the board.<br />Example: `{{ mled.FillColor "Red" }}` produces an all red MLED display|

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

## Examples

All examples can be seen [here](../../scripting/examples.md).