## /vessels/<RegExp>/environment

*undefined*
Schema describing the environmental child-object of a Vessel.

* Type: `object`
* Path: `/vessels/(^urn:mrn:(imo|signalk):(mmsi:[2-7][0-9]{8,8}|uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}))|^(http(s?):.*|mailto:.*|tel:(\+?)[0-9]{4,})$/environment`
* Node: `environment`

### Source:
```
{
  "type": "object",
  "$schema": "http://json-schema.org/draft-04/schema#",
  "id": "https://signalk.github.io/specification/schemas/groups/environment.json#",
  "description": "Schema describing the environmental child-object of a Vessel.",
  "title": "environment",
  "definitions": {
    "objectWithTemperature": {
      "type": "object",
      "properties": {
        "temperature": {
          "description": "Temperature",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "K"
        }
      }
    }
  },
  "properties": {
    "outside": {
      "type": "object",
      "properties": {
        "temperature": {
          "description": "Current outside air temperature",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "K"
        },
        "dewPointTemperature": {
          "description": "Current outside dew point temperature",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "K"
        },
        "apparentWindChillTemperature": {
          "description": "Current outside apparent wind chill temperature",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "K"
        },
        "theoreticalWindChillTemperature": {
          "description": "Current outside theoretical wind chill temperature",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "K"
        },
        "heatIndexTemperature": {
          "description": "Current outside heat index temperature",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "K"
        },
        "pressure": {
          "description": "Current outside air ambient pressure",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "Pa"
        },
        "humidity": {
          "description": "Current outside air relative humidity",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "ratio"
        }
      }
    },
    "inside": {
      "type": "object",
      "properties": {
        "temperature": {
          "description": "Current inside air temperature",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "K"
        },
        "humidity": {
          "description": "Current inside air relative humidity",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "ratio"
        },
        "engineRoom": {
          "description": "Current engine room air temperature",
          "$ref": "#/definitions/objectWithTemperature"
        },
        "mainCabin": {
          "description": "Current main cabin air temperature",
          "$ref": "#/definitions/objectWithTemperature"
        },
        "refrigerator": {
          "description": "Current refrigerator temperature",
          "$ref": "#/definitions/objectWithTemperature"
        },
        "freezer": {
          "description": "Current freezer temperature",
          "$ref": "#/definitions/objectWithTemperature"
        },
        "heating": {
          "description": "Current heating temperature",
          "$ref": "#/definitions/objectWithTemperature"
        }
      }
    },
    "water": {
      "type": "object",
      "properties": {
        "temperature": {
          "description": "Current water temperature",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "K"
        },
        "salinity": {
          "description": "Water salinity",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "ratio"
        },
        "liveWell": {
          "description": "Current livewell temperature",
          "$ref": "#/definitions/objectWithTemperature"
        },
        "baitWell": {
          "description": "Current baitwell air temperature",
          "$ref": "#/definitions/objectWithTemperature"
        }
      }
    },
    "depth": {
      "title": "depth",
      "type": "object",
      "description": "Depth related data",
      "properties": {
        "belowKeel": {
          "description": "Depth below keel",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m"
        },
        "belowTransducer": {
          "description": "Depth below Transducer",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m"
        },
        "belowSurface": {
          "description": "Depth from surface",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m"
        },
        "transducerToKeel": {
          "description": "Depth from the transducer to the bottom of the keel",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m"
        },
        "surfaceToTransducer": {
          "description": "Depth transducer is below the water surface",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m"
        }
      }
    },
    "current": {
      "type": "object",
      "title": "current",
      "description": "Direction and strength of current affecting the vessel",
      "allOf": [
        {
          "$ref": "../definitions.json#/definitions/commonValueFields"
        },
        {
          "properties": {
            "drift": {
              "type": "number",
              "description": "The speed component of the water current vector",
              "example": 3.12,
              "units": "m/s"
            },
            "setTrue": {
              "type": "number",
              "description": "The direction component of the water current vector referenced to true (geographic) north",
              "example": 123.45,
              "units": "rad"
            },
            "setMagnetic": {
              "type": "number",
              "description": "The direction component of the water current vector referenced to magnetic north",
              "example": 131.22,
              "units": "rad"
            }
          }
        }
      ]
    },
    "tide": {
      "type": "object",
      "title": "tide",
      "description": "Tide data",
      "properties": {
        "heightHigh": {
          "description": "Next high tide height  relative to lowest astronomical tide (LAT/Chart Datum)",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m"
        },
        "heightNow": {
          "description": "The current tide height  relative to lowest astronomical tide (LAT/Chart Datum)",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m"
        },
        "heightLow": {
          "description": "The next low tide height relative to lowest astronomical tide (LAT/Chart Datum)",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m"
        },
        "timeLow": {
          "description": "Time of the next low tide in UTC",
          "$ref": "../definitions.json#/definitions/timestamp"
        },
        "timeHigh": {
          "description": "Time of next high tide in UTC",
          "$ref": "../definitions.json#/definitions/timestamp"
        }
      }
    },
    "heave": {
      "description": "Vertical movement of the vessel due to waves",
      "$ref": "../definitions.json#/definitions/numberValue",
      "units": "m"
    },
    "wind": {
      "type": "object",
      "title": "wind",
      "description": "Wind data.",
      "properties": {
        "angleApparent": {
          "description": "Apparent wind angle, negative to port",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "rad"
        },
        "angleTrueGround": {
          "description": "True wind angle based on speed over ground, negative to port",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "rad"
        },
        "angleTrueWater": {
          "description": "True wind angle based on speed through water, negative to port",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "rad"
        },
        "directionChangeAlarm": {
          "description": "The angle the wind needs to shift to raise an alarm",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "rad"
        },
        "directionTrue": {
          "description": "The wind direction relative to true north",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "rad"
        },
        "directionMagnetic": {
          "description": "The wind direction relative to magnetic north",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "rad"
        },
        "speedTrue": {
          "description": "Wind speed over water (as calculated from speedApparent and vessel's speed through water)",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m/s"
        },
        "speedOverGround": {
          "description": "Wind speed over ground (as calculated from speedApparent and vessel's speed over ground)",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m/s"
        },
        "speedApparent": {
          "description": "Apparent wind speed",
          "$ref": "../definitions.json#/definitions/numberValue",
          "units": "m/s"
        }
      }
    },
    "time": {
      "type": "object",
      "description": "A time reference onboard.",
      "properties": {
        "millis": {
          "type": "number",
          "title": "Epoch time",
          "example": 1449648657735,
          "description": "Milliseconds since the UNIX epoch (1970-01-01 00:00:00)"
        },
        "timezone": {
          "type": "number",
          "title": "Timezone offset",
          "example": -400,
          "maximum": 1300,
          "minimum": -1300,
          "description": "Timezone offset in hours and minutes (-)hhmm"
        },
        "timestamp": {
          "$ref": "../definitions.json#/definitions/timestamp"
        },
        "source": {
          "$ref": "../definitions.json#/definitions/source"
        }
      }
    },
    "mode": {
      "type": "object",
      "description": "Mode of the vessel based on the current conditions. Can be combined with navigation.state to control vessel signals eg switch to night mode for instrumentation and lights, or make sound signals for fog.",
      "properties": {
        "value": {
          "enum": [
            "day",
            "night",
            "restricted visibility"
          ]
        },
        "timestamp": {
          "$ref": "../definitions.json#/definitions/timestamp"
        },
        "source": {
          "$ref": "../definitions.json#/definitions/source"
        }
      }
    }
  }
}
```

---