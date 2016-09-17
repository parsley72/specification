## /vessels/<RegExp>/navigation/lights

*undefined*
Current state of the vessels navigation lights

* Type: `object`
* Path: `/vessels/(^urn:mrn:(imo|signalk):(mmsi:[2-7][0-9]{8,8}|uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}))|^(http(s?):.*|mailto:.*|tel:(\+?)[0-9]{4,})$/navigation/lights`
* Node: `lights`

### Source:
```
{
  "type": "object",
  "title": "Navigation lights",
  "description": "Current state of the vessels navigation lights",
  "properties": {
    "value": {
      "type": "string",
      "enum": [
        "off",
        "fault",
        "anchored",
        "sailing",
        "motoring",
        "towing < 200m",
        "towing > 200m",
        "pushing",
        "fishing",
        "fishing-hampered",
        "trawling",
        "trawling-shooting",
        "trawling-hauling",
        "pilotage",
        "not-under-way",
        "aground",
        "restricted manouverability",
        "restricted manouverability towing < 200m",
        "restricted manouverability towing > 200m",
        "restricted manouverability underwater operations",
        "constrained by draft",
        "mine clearance"
      ]
    },
    "source": {
      "description": "Source of this data",
      "$ref": "../definitions.json#/definitions/source"
    },
    "timestamp": {
      "description": "timestamp of the last update to this data",
      "$ref": "../definitions.json#/definitions/timestamp"
    }
  }
}
```

---