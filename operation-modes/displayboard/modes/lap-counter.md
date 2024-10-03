# Lap Counter

RRExchange can be used as a basic lap counter, allowing to count up or down including a total lap count.&#x20;

## Keyboard bindings

Besides manually clicking the laps in the user interface, you can also use keyboard bindings. In ? - Command Bindings there are the following options:&#x20;

| Name     | Description                         |
| -------- | ----------------------------------- |
| Lap      | Binding for triggering a lap change |
| Lap Down | Binding for counting a lap down     |
| Lap Up   | Binding for countiong a lap up      |

## Impulses

If you want to use a pushbutton connected to a timing device, you can add the timing device in the Impulses Push view and make sure that your pushbutton impulse is coming in and on whioch channel. You can then enter the channel name in the kexyboard bindings window:

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Channel names can be entered with an additional port numer and "/" in the front - this way only the respective channel on the timing device on the port number will trigger.

## Script

A typical lap counter script will show the current lap and the total laps.

```
{{ Laps | TrimPad 4 "Center" }}{{ TotalLaps | TrimPad 4 "Center" }}
```
