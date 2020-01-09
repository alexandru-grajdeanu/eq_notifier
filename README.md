## Earthquake notifier


This projects aims to send an SMS to a specific number (using [Twilio](https://www.twilio.com/)) if an earthquake with magnitude > 4 
is going to occur (depending on your location, this can warn you -*best scenario*- within 25-30 seconds before you feel
the earthquake wave).

---

## Info

This simple script was mainly done for testing purposes and learning activities. **DO NOT** take the information for granted as there might be big delays between the time the earthquake occurs and the time the SMS arrives.

More, this works only for *Romania, Europe* and it's using the data from [this website](http://alerta.infp.ro) which is in a testing phase (BETA). 

---

## Script details

* Python 3.6

To run this on your local machine:

```
> git clone https://github.com/alexandru-grajdeanu/eq_notifier.git
> cd eq_notifier/
> pip install -r requirements.txt  # At this point, you'll have to create a twilio account (which is free) and set it up
> touch credentials.json  # in this file you'll put the details you need (see `get_secrets()` method for an example)
> python eq_notifier.py 
```

There's also the possibility of using CLI arguments:

- `twilio` (path to the credentials file)
- `delay` (delay in seconds between two calls to the earthquake API)