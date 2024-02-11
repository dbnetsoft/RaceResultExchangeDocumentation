# Timetrial

This mode is suitable for showing a running time for a specific competitor that passes an announcement line or is manually select and then show the result whenever the athlete cross the next timing point. When several athletes cross the timing point in short intervals, the passings are queued up and the interval can be specified when switching.

For this to work oyu have to setup the following:

* For being able to calculate a running time, RRExchange needs to know the StartTOD of the athlete. Specify the field name that contains the TOD.
* Select the announcement timing point to listen to for passings that are then set to next to finish
* Select the timing point to listen to for passings to show the passings
* Enter the duration for switching from passings mode to idle mode (e.g. 5s after a passing happened fall back to idle mode)
* Enter the duration for switching between passings if more than one is queued up (e.g. 3s to faster iterate through the queue)
* Select a mode to display when idle, meaing when no passing happened.

The timetrial templazte will be used before the finish, the passings template will be used when finished.

In the box on the right you see the bib numbers are currently queued up at the finish and also queued up for arriving next at the finish.

<figure><img src="https://dbnetsoft.github.io/RaceResultExchangeDocumentation/displayboards/modes/timetrial/timetrial.png" alt=""><figcaption></figcaption></figure>
