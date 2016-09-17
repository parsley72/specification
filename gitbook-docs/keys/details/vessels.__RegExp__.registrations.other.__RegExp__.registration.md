## /vessels/<RegExp>/registrations/other/<RegExp>/registration

The registration code

* Type: `string`
* Path: `/vessels/(^urn:mrn:(imo|signalk):(mmsi:[2-7][0-9]{8,8}|uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}))|^(http(s?):.*|mailto:.*|tel:(\+?)[0-9]{4,})$/registrations/other/(^[A-Za-z0-9_-]+$)/registration`
* Node: `registration`

### Example:
```
DOC-2345
```

### Source:
```
{
  "type": "string",
  "description": "The registration code",
  "example": "DOC-2345"
}
```

---