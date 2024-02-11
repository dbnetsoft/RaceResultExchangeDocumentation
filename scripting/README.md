# Scripting

RaceResultExchange comes with a powerful template/scripting engine.

The procedure when processing a script is always the same:

1. Fields from RR12 enclosed in square brackets are retrieved from RR12 (e.g. `[LastName]`) and replaced with the placeholder.
2. The scripting engine runs and formats the output.

### RR12 Fields <a href="#rr12-fields" id="rr12-fields"></a>

Standard fields (e.g. for timing point), User-defined fields or User-defined functions can be requested from RR12 by putting the variable name in square brackets. E.g. pulling the lastname from RR12 you need to write `[LastName]`. You can also write `[GetStageResult(1)]` to access a user-defined function. In case you want to use the value inside a script, you have to make sure to include string values with surrounded quotation marks like this `{{ lastnameVariable = "[LastName]" }}`.

### Scripting <a href="#scripting_1" id="scripting_1"></a>

Scripting is based on the powerful [Scriban scripting language](https://github.com/scriban/scriban). You can find more information here:

* Language Overview: [Here](https://github.com/scriban/scriban/blob/master/doc/language.md)
* Built-in Functions: [Here](https://github.com/scriban/scriban/blob/master/doc/builtins.md)

Different than stated in the scriban docs, Race Result Exchange is not changing the casing of variables or functions. Even more, you can use `string.ends_with`or `string.EndsWith`, whereas the later is preferred as it means the declaration of the method is not touched.

The following script will output "Hello World":

```
{{ "Hello World" }}
```

The following script will modify the field from RR12 and pads it to 12 characters and center aligns it if need be. This is possible by using the `|` pipe character: The expression to the left is forwasrded to a function that is given by the name after the pipe. The forwarded argument will be the first in the function arguments list:

```
{{ "[LastName]" | TrimPad 12 "Center" }}
```

Without using piping, you can also use a traditional way of calling methods:

```
{{ TrimPad "[LastName]" 12 "Center" }}
```
