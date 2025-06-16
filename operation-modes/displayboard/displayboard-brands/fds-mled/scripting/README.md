# Scripting

## Examples <a href="#examples" id="examples"></a>

All examples can be seen[ here](../../../../../scripting/examples/).

## Alternative

Insteaf of using the built-in _FDS MLED_ device that allows to specifiy line nr and script, one can also use the _Custom_ display device.&#x20;

In order to create an output on the FDS MLED, one can use the mled.CreateProtocol function. An example is this script

```
{{
now = date.Now
if now.Second  %2 == 0
    nowString = now | Format "HH:mm"
else
    nowString = now | Format "HH mm"
end
nowString = nowString | TrimPad 8 "Center"

# This will generate an FDS MLED compatible output
mled.CreateProtocol nowString 1 "Bright" 
}}
```
