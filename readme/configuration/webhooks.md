# WebHooks

Web Hooks need only to be created when you want to use the [Triggered Action](../../operation-modes/triggered-actions.md) feature (e.g. print a bib when new competitor is created) on participant changes.

Depending whether you work online or offline, your RR12 event needs to be configured slightly different.

## Online

Our RemoteRedirect webservice provides a bridge between RR12 working online that can only access public web servers and RRExchange running locally.&#x20;

{% hint style="info" %}
Protocol is https and host is raceresult.remoteredirect.com:\
`https://raceresult.remoteredirect.com`
{% endhint %}

The following web hooks need to be configured in RR12 (Main Window - Access Rights/Simplae API - Web Hooks):

<table><thead><tr><th width="138">Type</th><th>URL</th><th width="96">Filter</th><th>Fields</th></tr></thead><tbody><tr><td>New Participant</td><td><a href="https://raceresult.remoteredirect.com/api/raceresult/newparticipant">https://raceresult.remoteredirect.com/api/raceresult/newparticipant</a></td><td></td><td>ID;Bib;Lastname</td></tr><tr><td>Participant updated</td><td><a href="https://raceresult.remoteredirect.com/api/raceresult/updateparticipant">https://raceresult.remoteredirect.com/api/raceresult/updateparticipant</a></td><td></td><td>ID;Bib;Lastname</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (3).png" alt="" width="375"><figcaption><p>RR12 Configuration when working online</p></figcaption></figure>

## Offline

When working offline (e.g. checking out the event and using the local race result Web Server, RRExchange acts a a server to receive web hooks.

{% hint style="info" %}
Protocol is http (not https) and host is localhost:8181 (no www, take care with the :):\
`http://localhost:8181`
{% endhint %}

The following web hooks need to be configured in RR12 (Main Window - Access Rights/Simple API - Web Hooks):

<table><thead><tr><th width="138">Type</th><th>URL</th><th width="96">Filter</th><th>Fields</th></tr></thead><tbody><tr><td>New Participant</td><td><a href="http://localhost:8181">http://localhost:8181</a>/<a href="https://raceresult.remoteredirect.com/api/raceresult/newparticipant">api/raceresult/newparticipant</a></td><td></td><td>ID;Bib;Lastname</td></tr><tr><td>Participant updated</td><td><a href="http://localhost:8181">http://localhost:8181</a>/<a href="https://raceresult.remoteredirect.com/api/raceresult/updateparticipant">api/raceresult/updateparticipant</a></td><td></td><td>ID;Bib;Lastname</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (1).png" alt="" width="375"><figcaption><p>RR12 Configuration when working offline</p></figcaption></figure>
