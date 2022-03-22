# Formatting

## General

Placeholders can be inserted similar to RaceResult 12 by surrounding special field names with `[ ]`, e.g. `[clock]`. 

## Formatting

The placeholders can be modified by using formatters that follow with a `:` after the field name, e.g. `[clock:8,c]` will align the clock field center within 8 characters. The available options are: 

* `[{fieldName}:{count},{alignment}]` where count is the number of characters (trimmed if longer or padded if shorter) and the alignment within (`r` for right aligned, `c` for center aligned and `l` for left aligned)

## Placeholders

You can use the following placeholders everywhere: 

* `clock` contains the current time of day
* `countdown` contains the countdown to the given target time
* `runtime` contains the running time from the given target time
* `textline{x}]` contains the freetext lines, replace {x} with your line number starting from 1

In Time trial mode, the following placeholders can be used in addition: 

* `runningtime` contains the running time of the athlete expected next to finish (calculated locally by using the field specified in "Start TOD Field")

All other fields will be pulled from RR12 and depends on your event file configuration.

## Colors

FDS MLED panels also support setting colors. You can find the specific codes needed in the FDS MLED manual. You can send `^cs 2^Welcome^cs 0^` to show Welcome text in green color.