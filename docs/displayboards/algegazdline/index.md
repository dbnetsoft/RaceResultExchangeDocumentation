# ALGE-Timing GAZ/Dline

## Setup

ALGE-Timing GAZ/Dline displayboards provide a single, addressable line for displaying rank, bib and time simulatenously.

The following operation modes are provided: 

* `Clear` shows the clear template (usually is for blanking the board)
* `Clock` shows the clock template (usually  is for showing current time of day)
* `Text` shows the freetext template 
* `Countdown`shows the countdown template (usually for counting down to a target time)
* `Runtime` shows the runtime template (usually for running up from a target time)
* `Passings` shows the passings template
* `Timetrial` shows the time trial template

Templates can contain any information, but it is good practice to at least show what it is supposed to show (e.g. one can show blank in the clock template, but it makes sense to show a clock there).

The operation modes can be switched to by selecting them: 
![Screenshot](../switchingmodes.png)

## Templates

The templates for each mode can be edited by clicking on the Pen button next to each select box. 

Each addressable template can contain seperate text for bib, rank or time part of the display. 
Please see the [scripting](scripting.md) for further details on how to format fields specially for the GAZ/DLines.

![Screenshot](../edittemplate.png)

