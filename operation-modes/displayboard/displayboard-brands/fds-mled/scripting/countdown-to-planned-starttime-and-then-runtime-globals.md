# Countdown to planned starttime and then runtime (Globals)

The following script allows to show the countdown to the planned starttime from the contest and then a runtime during the race.

This can be achieved by having the race start TOD and the planned start TOD available in a RR12 list. The actual content of these values depend on your event file setup.

<figure><img src="../../../../../.gitbook/assets/image (18).png" alt="" width="357"><figcaption></figcaption></figure>

This list is then pulled via RRExchange globals feature periodically into the software.

<figure><img src="https://dbnetsoft.github.io/RaceResultExchangeDocumentation/scripting/globals.png" alt="" width="375"><figcaption></figcaption></figure>

The pulled global list entries are available as variables in each script then. They are identified by the name of the global. Also you can shortcut to the first row by using `.First`., e.g. `GlobalsName.First.Starttime` for a RR12 field named `Starttime` in a globals list `GlobalsName`.

```
{{ 
now = Clock.TimeOfDay.TotalSeconds
plannedStarttime = GlobalsName.First.PlannedStarttime | ToSeconds
actualStarttime = GlobalsName.First.Starttime  | ToSeconds

# Check for if an actual start time is set
if (actualStarttime == 0) 
    # Countdown to planned start time
    
    # Calculate duration until start
    durationUntilStart = plannedStarttime - now
    
    # If duration has elapsed but no actual starttime is present, stay at 0
    if (durationUntilStart < 0)
        durationUntilStart = 0
    end    
    
    # Format countdown time
    displayText = durationUntilStart | FormatRaceResult "HH:Mm:ss"   
   
      # Output countdown in red
    colorString = "Red"
else 
    # Runtime after actual start time
     
     # Calculate runtime since actual start
     elapsedSinceStart = now - actualStarttime
     
      # Format runtime
      displayText = elapsedSinceStart | FormatRaceResult "HH:Mm:ss"
     
      # Output runtime in green
    colorString = "Green"
end

(mled.Color colorString) + (TrimPad displayText 8 "Right")
}}
```
