## /vessels/<RegExp>/sails/inventory/<RegExp>/active

Indicates wether this sail is currently in use or not

* Type: `boolean`
* Path: `/vessels/(^urn:mrn:(imo|signalk):(mmsi:[2-7][0-9]{8,8}|uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}))|^(http(s?):.*|mailto:.*|tel:(\+?)[0-9]{4,})$/sails/inventory/(^[a-zA-Z0-9]+$)/active`
* Node: `active`

### Source:
```
{
  "type": "boolean",
  "description": "Indicates wether this sail is currently in use or not"
}
```

---