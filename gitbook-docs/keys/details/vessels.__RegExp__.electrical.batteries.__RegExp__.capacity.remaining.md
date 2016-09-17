## /vessels/<RegExp>/electrical/batteries/<RegExp>/capacity/remaining

Capacity remaining in battery

* Type: `number`
* Path: `/vessels/(^urn:mrn:(imo|signalk):(mmsi:[2-7][0-9]{8,8}|uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}))|^(http(s?):.*|mailto:.*|tel:(\+?)[0-9]{4,})$/electrical/batteries/(^[A-Za-z0-9]+$)/capacity/remaining`
* Node: `remaining`

### Source:
```
{
  "type": "number",
  "description": "Capacity remaining in battery",
  "units": "J"
}
```

---