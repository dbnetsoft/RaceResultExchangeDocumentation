# Scripting

## General

RaceResultExchange comes with a powerful template/scripting engine. 

The procedure when processing a script is always the same:

1. Fields from RR12 enclosed in square brackets are retrieved from RR12 (e.g. `[LastName]`) and replaced with the placeholder. 
2. The scripting engine runs and formats the output. 

## RR12 Fields

Standard fields (e.g. for timing point), User-defined fields or User-defined functions can be requested from RR12 by putting the variable name in square brackets. E.g. pulling the lastname from RR12 you need to write `[LastName]`. You can also write `[GetStageResult(1)]` to access a user-defined function.

## Scripting

Scripting is based on the powerful [Scriban scripting language](https://github.com/scriban/scriban). You can find more information on the language features [here](https://github.com/scriban/scriban/blob/master/doc/language.md). More information on built-in functions can be found [here](https://github.com/scriban/scriban/blob/master/doc/builtins.md).

The following script will just pull the field `[LastName]` from RR12 and outputs it:

    [LastName]

The following script will modify the field from RR12 and pads it to 12 characters and center aligns it if need be. This is possible by using the | pipe character: The expression the left is forwasrded to a function that is given by the name after the pipe. 

    {{ [LastName] | trim_pad 12 "Center" }}




