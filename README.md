# Python-TStat
Python interface for Radio Thermostat wifi-enabled thermostats.

#Usage:
t = TStat('1.2.3.4')         Where 1.2.3.4 is your thermostat's IP address

t.getCurrentTemp()           Returns current temperature as a float

t.setHeatPoint(68.0)         Sets target temperature for heating to 68.0

...

A simple cache based on retrieved URL and time of retrieval is included.
If you call TStat.getFanMode(), /tstat will be retrieved and the value
for fmode will be return.  If you then call t.getTState(), a cached
value will already exist and tstate will be returned from that.

You can change the time for cache expiration by calling

t.setCacheExpiry(timeInSeconds).
