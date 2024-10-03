# Clock w/ flashing seperators



The current clock is captured in the variable `now`. Then we compare the datetime's Second property and see if it is even. Depending on the output of this comparison the clock is formatted with different formatters. Either way, the last line trim's the output and aligns it center.

```
{{
now = date.Now
if now.Second  %2 == 0
    nowString = now | Format "HH:mm"
else
    nowString = now | Format "HH mm"
end
nowString | TrimPad 8 "Center"
}}
```
