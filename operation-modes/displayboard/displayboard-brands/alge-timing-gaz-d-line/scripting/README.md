# Scripting

### Rank and bib <a href="#rank-and-bib" id="rank-and-bib"></a>

GAZ/DLines can show rank and bib simultaneously together with the time. However, bib can only be three digits and rank only two digits. Therefore it is best to format the fields pulled from RR12 accordingly:

* Bib: `{{ [Bib] | TrimPad 3 "Center" }}` to trim it to three digits and align center
* Rank: `{{ [RankFieldFromRR12] | TrimPad 2 "Center" }}` to trim it to two digits and align center. Best is for the field to only contain the number, no formatter like a period at the end of the rank.

### Time <a href="#time" id="time"></a>

GAZ/DLines expect a very specific format for it show information on it at all. Therefore besides properly formatting bib and rank, also the time needs to be formatted in a special way. Therefore some helper functions come in handy:

### &#x20;<a href="#functions" id="functions"></a>
