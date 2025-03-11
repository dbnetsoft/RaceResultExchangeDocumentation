# HTTP GET JSON

RR12 lists will be fetched peridocally and made available by its name.&#x20;

The following properties are available on the object:

| Property   | Description                                                         |
| ---------- | ------------------------------------------------------------------- |
| Name       | Name of the list                                                    |
| Url        | Url of the list                                                     |
| Data       | The parsed JSON data. This can either be an object or an array/list |
| StatusCode | Should be 200 for a good response                                   |
| IsValid    | true when response is valid                                         |
| First      | First element in case Data is an array/list                         |
| ListCount  | Numer of items in the list in case Data is an array/list            |
| UpdatedAt  | Timestamp when the list was updated and fetched from server         |
