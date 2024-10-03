# Clock w/ flashing seperator

The current clock is captured in the variable `now`. Then we compare the datetime's Second property and see if it is even. Depending on the output of this comparison the clock is formatted with different formatters. Also also not showoing seconds.

{% code title="Time Script" %}
```
{{
# capture current time in variable now
now = date.Now

# depending on second, either with or without :
if now.Second  %2 == 0
    nowString = now | Format "HH:mm"
else
    nowString = now | Format "HH mm"
end

# variable to switch between output on the hour:min or min:sec digits 
outputAsHours = false
if (outputAsHours)
    # append with blanks for :00.000
    nowString = nowString + "       "
else 
    # prepend with HH: and append with .000
        nowString = "   " + nowString + "    "
end
nowString
}}
```
{% endcode %}

