# Clock & Runtime

If you want to show the clock, when no event is started and show the runtime based on the latest event that is started, you can create a globals output list like and a custom script

## Output List

Grouping/sorting: Sort by T0 descending.

Max Records: 1

Filter: Time0 <> "" and Time0 <> your fake starttime

| Column Heading | Data  | Info |
| -------------- | ----- | ---- |
| T0             | Time0 |      |

Script

In the Runtime section, enter the following script for the time:

```
{{
# Get current TOD and convert to seconds
now = timespan.Now | ToSeconds

if (Globals.First != null) 

   # Fetch race start time and winner time from Globals List and convert to seconds (this way RR12 field can be seconds or HH:mm:ss string
   raceStartedAt = Globals.First.T0 | ToSeconds

   # Determine race states
   isRaceStarted = raceStartedAt > 0

   # Determine output based on is race started or not
   if isRaceStarted 
   
      # Calculate runtime
      timeSinceStart = now - raceStartedAt
      
      # Show runtime formatted
      timeSinceStart | gaz.Format "Seconds" false
   
   else 
       # Before Start
       
       # Show clock
      now | gaz.Format "Seconds" false
   
   end
   
else 
   # No contest started yet - show clock

   now | gaz.Format "Seconds" false
   
 end

}}
```
