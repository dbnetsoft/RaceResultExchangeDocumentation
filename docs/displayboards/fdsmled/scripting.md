# Scripting

## Colors

FDS MLED panels also support setting colors. 

The following functions are available: 

* `mled.Color "ColorName"`: This function will start a new color for the following text.
* `mled.EndColor`: This function will end the latest color changed and fall back to the default panel color.
* `mled.FillColor "ColorName"`: This function will change the background color of the board.

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

Showing the current time of day with only hours and minutes in red: `{{ mled.Color "Red" }}{{ Clock | Format "HH:mm" }}`