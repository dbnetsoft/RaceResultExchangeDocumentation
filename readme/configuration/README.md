# Configuration

## Configuration <a href="#configuration" id="configuration"></a>

A couple of steps have to be done in order to link RaceResult12 and RaceResultExchange.

### Link Race Result Account and Event <a href="#link-race-result-account-and-event" id="link-race-result-account-and-event"></a>

This settings can be found in `File` - `Settings`:

* The Customer ID is bound to yur license and already pre-filled
* Enter the password for this customer ID in RR12
* Select if you want to use an event that is online or offline. When working offline please specify the IP address of the computer running RR12 or `localhost` for the same machine
* Select an event to be working with (you can also select the event from the Main window)

Most settings need to be done in the software itself (`Settings` button in the navigation panel to the left), some settings directly in Race Result 12.

<figure><img src="../../.gitbook/assets/configuration_linkrr.png" alt=""><figcaption><p>Settings Dialog</p></figcaption></figure>

### Setup Race Result Event <a href="#setup-race-result-event" id="setup-race-result-event"></a>

The RR12 event does not need to be setup with Simple API to pull data.&#x20;

However, you might want to setup [web hooks ](webhooks.md)(for acting upon participant changes) or [exporters ](exporter.md)(for acting upon new raw data).&#x20;

<figure><img src="../../.gitbook/assets/image (5).png" alt="" width="375"><figcaption></figcaption></figure>
