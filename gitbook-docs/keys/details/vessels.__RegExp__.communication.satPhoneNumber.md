## /vessels/<RegExp>/communication/satPhoneNumber

Satellite phone number for vessel.

* Type: `string`
* Path: `/vessels/(^urn:mrn:(imo|signalk):(mmsi:[2-7][0-9]{8,8}|uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}))|^(http(s?):.*|mailto:.*|tel:(\+?)[0-9]{4,})$/communication/satPhoneNumber`
* Node: `satPhoneNumber`

### Example:
```
+64xxxxxx
```

### Source:
```
{
  "type": "string",
  "description": "Satellite phone number for vessel.",
  "example": "+64xxxxxx"
}
```

---