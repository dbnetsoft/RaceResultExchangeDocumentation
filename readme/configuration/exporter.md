# Exporter

Exporters need to be created when you want to have RRExchange react upon the arrival of new passings, e.g. show rank and time on a display board or trigger a HTTP post message.&#x20;

In order to receive raw data passings and RRExchange can act upon them (e.g. to display rank and time on a displayboard or to trigger a HTTP POST), RR12 exchange needs to define an exporter to send data to us.&#x20;

## Online

Our RemoteRedirect webservice provides a bridge between RR12 working online that can only access public web servers and RRExchange running locally.&#x20;

{% hint style="info" %}
Protocol is https and host is raceresult.remoteredirect.com:\
`https://raceresult.remoteredirect.com`
{% endhint %}

The following exporter need to be configured in RR12 (Timing - Exporters & Tracking - Exporters):

| URL                                                                                                                                                 | Export Data                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| <p>HTTP(S) Post</p><p>h<a href="http://localhost:8181/api/raceresult/exporter">ttps://raceresult.remoteredirect.com/api/raceresult/exporter</a></p> | <p>Custom<br><code>[RD_TimingPoint]&#x26;";"&#x26;[Bib] &#x26; ";" &#x26; [Event.ID]</code></p> |



## Offline

When working offline (e.g. checking out the event and using the local race result Web Server, RRExchange acts a REST API server to receive exporter data.

{% hint style="info" %}
Protocol is http (not https) and host is localhost:8181 (no www, take care with the :):\
`http://localhost:8181`
{% endhint %}

| URL                                                                                                                                 | Export Data                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| <p>HTTP(S) Post</p><p>h<a href="http://localhost:8181/api/raceresult/exporter">ttp://localhost:8181/api/raceresult/exporter</a></p> | <p>Custom<br><code>[RD_TimingPoint]&#x26;";"&#x26;[Bib] &#x26; ";" &#x26; [Event.ID]</code></p> |

## Online & Offline

_Name_ can be defined as you like, e.g. RRExchange. _Timing Point/Split_ and _Filter_ can be set to whatever you need, however you can always filter in RRExchange as well - so best is to leave it on _All_.&#x20;
