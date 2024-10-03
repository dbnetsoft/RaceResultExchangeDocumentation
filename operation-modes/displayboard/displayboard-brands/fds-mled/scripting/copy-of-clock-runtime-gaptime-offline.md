# Clock, Runtime, Gaptime (Offline)

The following script allows to show the current clock before the start of the race, a runtime during the race and a gap time to winner as soon as the first athlete finishes.&#x20;

Instead of pulling the race start TOD and winner time from RR12[ via globals](clock-runtime-gaptime-globals.md), we use the manual buttoins in the user interface. his list is then pulled via RRExchange globals feature periodically into the software.

```
{{
# Get current TOD and convert to seconds
now = timespan.Now | ToSeconds

# Fetch race start time and winner time from Globals List and convert to seconds (this way RR12 field can be seconds or HH:mm:ss string
raceStartedAt = ReferenceTime | ToSeconds
winnerFinishedAt = GapReferenceTime  | ToSeconds

# Determine race states
isRaceStarted = raceStartedAt > 0

# Determine output based on is race started or not
if isRaceStarted 
    # Race is started, check for winner time is present    
    isWinnerFinished = winnerFinishedAt > 0

    if (isWinnerFinished)
        # Winnner is finished, show gap time

        # Change color
        mled.Color "Red"

        # Calculate gap time
        timeSinceWinner = now - winnerFinishedAt
        # Output formatted with + sign, trim to 8 places and right-align
        timeSinceWinner | FormatRaceResult "+HH:Mm:ss" | TrimPad 8 "Right"

    else 
        # No winner present, show running time

        # Change color
        mled.Color "Green"

        # Calculate runtime
        timeSinceStart = now - raceStartedAt
        # Output formatted, trim to 8 places and right-align
        timeSinceStart | FormatRaceResult "HH:Mm:ss" | TrimPad 8 "Right"

    end

else 
    # Before Start

    # Switch to White
    mled.Color "White"

    # Output formatted, trim to 8 places and right-align
    now | FormatRaceResult "hh:mm:ss" | TrimPad 8 "Right"


end
}}
```
