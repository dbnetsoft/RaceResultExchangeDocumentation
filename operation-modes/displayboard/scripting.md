# Scripting

See [scripting ](../../scripting/)for further details on how scripting and placeholders work.

### Internal Fields <a href="#internal-fields" id="internal-fields"></a>

The following fields are available in all display board templates, not only the currently selected one:

* `Clock` contains the current time of day. E.g. one can use `{{ Clock | Format "HH:mm" }}` to format the clock with hours and minutes only.
* `Countdown` contains the countdown to the given target time
* `Runtime` contains the running time from the given target time
* `TextLine1`^, `TextLine2`, ... or `TextLines[x]` contains the freetext lines, replace x with your line number starting from 0
* `Gaptime` contains the current gap time to the leader if any, otherwise null
* `Leadertime` contains the current time of the leader if any, otherwise null

## Time Trial

In Time trial mode, the following fields can be used in addition:

* `RunningTime` contains the running time of the athlete expected next to finish (calculated locally by using the field specified in "Start TOD Field")

## Lap Counter

In lap counter mode, the following fields are available

_Lap_ holds the current lap, _Laps_ holds the total amount of laps.

