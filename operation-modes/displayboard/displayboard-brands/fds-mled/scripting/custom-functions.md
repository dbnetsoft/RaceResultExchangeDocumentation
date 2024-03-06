# Custom Functions



<table><thead><tr><th width="200">Method</th><th>Parameters</th><th>Description</th></tr></thead><tbody><tr><td><code>mled.Color</code></td><td><code>"ColorName"</code></td><td>This function will start a new color for the following text<br>Example: <code>{{ mled.Color "Red" }}Hello</code> produces the the text Hello in red font</td></tr><tr><td><code>mled.EndColor</code></td><td><code>&#x3C;string></code><br><code>&#x3C;length></code><br><code>"&#x3C;alignment>"</code></td><td>This function will end the latest color used and fall back to the default panel color.</td></tr><tr><td><code>mled.FillColor</code></td><td><code>"ColorName"</code></td><td>This function will change the background color of the board.<br>Example: <code>{{ mled.FillColor "Red" }}</code> produces an all red MLED display</td></tr></tbody></table>

Color names can be any of the following:

* Black
* Red
* Gree
* Blue
* Yellow
* Magenta
* Cyan
* White
* Orange
* DeepPink
* LightBlue
