# RR12 Lists

RR12 lists will be fetched peridocally and made available by its name.&#x20;

The following properties are available on the object:

| Property   | Description                                                       |
| ---------- | ----------------------------------------------------------------- |
| ListName   | Name of the list                                                  |
| List       | The parsed JSON data as an array                                  |
| StatusCode | Should be 200 for a good response                                 |
| IsValid    | true when response is valid                                       |
| First      | First element of the list if any                                  |
| ListCount  | Numer of items in the list                                        |
| UpdatedAt  | Timestamp on when the list was last updated and fetched from RR12 |

E.g. when you have a list define with name Test you can access the rows by using `Test.List` or access the third row with `Test.List[2]`.

E.g. a column named Starttime can be access for the first row by using `Test.First.Starttime`.

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
