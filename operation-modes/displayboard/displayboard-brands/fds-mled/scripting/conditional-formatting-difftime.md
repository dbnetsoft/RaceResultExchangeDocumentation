# Conditional formatting difftime

The diff field from RR12 is captured in the variable diffString. Then it is checked if the string starts with a "-". If so, set the color variable to green, otherwise to red. After that the color is output together with the diff string and trimmed.

```
{{ 
diffString = "+1.45"
colorString = ""
if string.StartsWith diffString "-"
    colorString = "Green"
else 
    colorString = "Red"
end
(mled.Color colorString) + (TrimPad diffString 8 "Right")
}}
```
