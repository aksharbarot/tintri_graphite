# tintri_graphite
Simple example to pull stats from a Tintri VMstore and pipe them to graphite.

![tintri_graphite dashboard](https://cloud.githubusercontent.com/assets/2933063/18573095/25030e30-7b86-11e6-9809-ef307bc17941.png "tintri_graphite dashboard")

## Requirements
1. Python
2. Tintri API examples

## Install
Download and install [Tintri's API examples](https://github.com/Tintri/tintri-api-examples) and place tintri_graphite.py in the same dir.  
## Usage
Simple call the script with the appropriate credentials as follows:

```
python graphite_tintry.py [vmstore_fqdn] [username] [password]
```

The script can be sent to the background or run with a screen session as it will poll the vmstore a set interval.  

You'll also need a storage schema stanza such as:

```
[tintri]
pattern = ^tintri\.
retentions = 5s:7d, 1m:30d, 15m:90d, 1h:3y
```

## Todo 
1. Capacity metrics
2. VM level metrics
3. Start/stop script
3. Better dashboard
