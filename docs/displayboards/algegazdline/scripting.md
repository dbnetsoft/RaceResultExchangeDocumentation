# Scripting

## Rank and bib

GAZ/DLines can show rank and bib simultaneously together with the time. However, bib can only be three digits and rank only two digits. Therefore it is best to format the fields pulled from RR12 accordingly: 

* Bib: `{{ [Bib] | TrimPad 3 "Center" }}` to trim it to three digits and align center
* Rank: `{{ [RankFieldFromRR12] | TrimPad 2 "Center" }}` to trim it to two digits and align center. Best is for the field to onlöy contain the number, no formatter like a period at the end of the rank.

## Time

GAZ/DLines expect a very specific format for it show information on it at all. Therefore besides properly formatting bib and rank, also the time needs to be formatted in a special way. Therefore some helper functions come in handy: 

* `ToTimeSpan` - takes the field from RR12 and converts it to a timespan. Therefore RR12 can submit a decimal time or a formatted time.
* `gaz.FormatTimeSpan "precision"` - this will format the converted timespan to a given precision and makes sure that the format matche the ALGE-Timing protocol.

`precision` can be any of the following enumeration: 

* `Seconds`
* `Tenths`
* `Hundredths`
* `Thousands`

Example:

`{{ "[RuntimeDisplayboard]" | ToTimeSpan | gaz.FormatTimeSpan "Hundredths"  }}`
