# Racemap

Racemap makes the data of it's trackers available via an easy Web API. This URL is individual per event.&#x20;

The data in this API contains each tracker's distance to start and from finish and many other data.&#x20;

## Get Distance from start from leading vehicles

In this example, we want to fetch the distance to finish from the lead vehicle's tracker.&#x20;

First we need to setup a global list with the URL provided by Racemap and name it _Racemap_:

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

In a script, we can now access the data via the _Racemap.Data_ variable. We loop through all trackers and find tghe one matching the lead vehicle tracker id. And then fetch the _toFinish_ property.&#x20;



```
{{
# Define tracker ID
leadTrackerId = "66bf4318d1c783279d183e37"
leadTrackerFound = false

# Loop through all trackers and pick the one we are interested in
for tracker in Racemap.Data.starters
    if (tracker.id == leadTrackerId)
        leadTrackerFound = true
        distanceToFinish = tracker.current.toFinish
    end
end

# Show texts based on distance
if leadTrackerFound
    if distanceToFinish > 0
        "Distance to Finish: " + ((distanceToFinish / 1000) | Format "####0.0") + "km"
     else 
       "Finished"
     end
else 
    "Tracker not found"
end
}}
```

