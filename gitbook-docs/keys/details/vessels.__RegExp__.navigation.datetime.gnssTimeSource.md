## /vessels/<RegExp>/navigation/datetime/gnssTimeSource

Source of GNSS Date and Time

* Type: `null`
* Path: `/vessels/(^urn:mrn:(imo|signalk):(mmsi:[2-7][0-9]{8,8}|uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}))|^(http(s?):.*|mailto:.*|tel:(\+?)[0-9]{4,})$/navigation/datetime/gnssTimeSource`
* Node: `gnssTimeSource`

### Source:
```
{
  "description": "Source of GNSS Date and Time",
  "enum": [
    "GPS",
    "GLONASS",
    "Galileo",
    "Beidou",
    "IRNSS",
    "Radio Signal",
    "Internet",
    "Local clock"
  ]
}
```

---