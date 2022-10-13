# Scripting

## Colors

FDS MLED panels also support setting colors. A lot of colors are possible to be used with FDS MLED boards, e.g. Red and Green or White. 

The following functions are available: 

* `mled.color "ColorName"`: This function will start a new color for the following text.
* `mled.end_color`: This function will end the latest color changed and fall back to the default panel color.
* `mled.fill_color "ColorName"`: This function will change the background color of the board.

Color names can be Red, Green, White or Blue.