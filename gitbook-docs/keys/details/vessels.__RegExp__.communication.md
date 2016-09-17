## /vessels/<RegExp>/communication

*undefined*
Schema describing the communication child-object of a Vessel.

* Type: `object`
* Path: `/vessels/(^urn:mrn:(imo|signalk):(mmsi:[2-7][0-9]{8,8}|uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}))|^(http(s?):.*|mailto:.*|tel:(\+?)[0-9]{4,})$/communication`
* Node: `communication`

### Source:
```
{
  "type": "object",
  "$schema": "http://json-schema.org/draft-04/schema#",
  "id": "https://signalk.github.io/specification/schemas/groups/communication.json#",
  "description": "Schema describing the communication child-object of a Vessel.",
  "title": "communication",
  "properties": {
    "callsignVhf": {
      "type": "string",
      "description": "Callsign for VHF communication",
      "example": "ZL1234"
    },
    "callsignHf": {
      "type": "string",
      "description": "Callsign for HF communication",
      "example": "ZL3RTH"
    },
    "phoneNumber": {
      "type": "string",
      "description": "Phone number of skipper",
      "example": "+64xxxxxx"
    },
    "emailHf": {
      "type": "string",
      "description": "Email address to be used for HF email (Winmail, Airmail, Sailmail)",
      "example": "motu@xxx.co.nz"
    },
    "email": {
      "type": "string",
      "description": "Regular email for the skipper",
      "example": "robert@xxx.co.nz"
    },
    "satPhoneNumber": {
      "type": "string",
      "description": "Satellite phone number for vessel.",
      "example": "+64xxxxxx"
    },
    "skipperName": {
      "type": "string",
      "description": "Full name of the skipper of the vessel.",
      "example": "Fabian Tollenaar"
    },
    "crewNames": {
      "type": "array",
      "description": "Array with the names of the crew",
      "items": [
        {
          "type": "string",
          "description": "Name of a crew member of the vessel.",
          "example": "Catherine"
        }
      ]
    }
  }
}
```

---