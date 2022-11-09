# Examples

## Clock with flashing separator

The current clock is captured in the variable `now`. Then we compare the datetime's Second property and see if it is even. Depending on the output of this comparison the clock is formatted with different formatters. Either way, the last line trim's the output and aligns it center.

    {{
    now = date.Now
    if now.Second  %2 == 0
        nowString = now | Format "HH:mm"
    else
        nowString = now | Format "HH mm"
    end
    nowString | TrimPad 8 "Center"
    }}

## Conditional formatting of diff time

The diff field from RR12 is captured in the variable diffString. Then it is checked if the string starts with a "-". If so, set the color variable to green, otherwise to red. After that the color is output together with the diff string and trimmed.

    {{ 
    var diffString = "[RR_Diff]"
    var colorString = ""
    if string.StartsWith diffString "-"
        colorCommand = "Green"
    else 
        colorString = "Red"
    end
    mled.Color colorString + TrimPad diffString 8 "Right"    
    }}