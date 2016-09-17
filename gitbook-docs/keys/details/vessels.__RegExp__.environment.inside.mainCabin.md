## /vessels/<RegExp>/environment/inside/mainCabin

* Type: `null`
* Path: `/vessels/(^urn:mrn:(imo|signalk):(mmsi:[2-7][0-9]{8,8}|uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}))|^(http(s?):.*|mailto:.*|tel:(\+?)[0-9]{4,})$/environment/inside/mainCabin`
* Node: `mainCabin`

### Source:
```
{
  "timestamp": {
    "type": "string",
    "description": "ISO-8601 (UTC) string representing date and time.",
    "units": "ISO-8601 (UTC)",
    "example": "2014-04-10T08:33:53Z"
  },
  "source": {
    "type": "object",
    "description": "Source of data, a record of where the data was received from. An object containing at least the properties defined in 'properties', but can contain anything beyond that.",
    "required": [
      "label",
      "type"
    ],
    "properties": {
      "label": {
        "type": "string",
        "description": "A label to identify the source bus, eg serial-COM1, eth-local,etc . Can be anything but should follow a predicatable format",
        "example": "N2K-1"
      },
      "type": {
        "type": "string",
        "description": "A human name to identify the type. NMEA0183, NMEA2000, signalk",
        "default": "NMEA2000",
        "example": "NMEA2000"
      },
      "src": {
        "type": "string",
        "description": "NMEA2000 src value or any similar value for encapsulating the original source of the data",
        "example": "36"
      },
      "pgn": {
        "type": "number",
        "description": "NMEA2000 pgn of the source message",
        "example": "130312"
      },
      "sentence": {
        "type": "string",
        "description": "Sentence type of the source NMEA0183 sentence, $GP[RMC],092750.000,A,5321.6802,N,00630.3372,W,0.02,31.66,280511,,,A*43",
        "example": "RMC"
      },
      "talker": {
        "type": "string",
        "description": "Talker id of the source NMEA0183 sentence, $[GP]RMC,092750.000,A,5321.6802,N,00630.3372,W,0.02,31.66,280511,,,A*43",
        "example": "GP"
      }
    }
  },
  "sourceRef": {
    "type": "string",
    "description": "Reference to the source under vessel's sources. A dot spearated path to the data. eg [type].[bus].[device]",
    "example": "NMEA0183.COM1.GP"
  },
  "version": {
    "type": "string",
    "description": "Version of the Signal K schema/APIs used by the root object.",
    "example": "1.0.0"
  },
  "units": {
    "type": "string",
    "description": "Allowed units of physical quantities. Units should be (derived) SI units where possible.",
    "properties": {
      "s": {
        "display": "s",
        "quantity": "Time",
        "quantityDisplay": "T",
        "description": "Elapsed time (interval) in seconds"
      },
      "Hz": {
        "display": "Hz",
        "quantity": "Frequency",
        "quantityDisplay": "F",
        "description": "Frequency in Hertz"
      },
      "m3": {
        "display": "m³",
        "quantity": "Volume",
        "quantityDisplay": "V",
        "description": "Volume in cubic meters"
      },
      "m3/s": {
        "display": "m3/s",
        "quantity": "Flow",
        "quantityDisplay": "Q",
        "description": "Liquid or gas flow in cubic meters per second"
      },
      "deg": {
        "display": "°",
        "quantity": "Angle",
        "quantityDisplay": "∠",
        "description": "Latitude or longitude in decimal degrees"
      },
      "rad": {
        "display": "㎭",
        "quantity": "Angle",
        "quantityDisplay": "∠",
        "description": "Angular arc in radians"
      },
      "rad/s": {
        "display": "㎭/s",
        "quantity": "Rotation",
        "quantityDisplay": "ω",
        "description": "Angular rate in radians per second"
      },
      "A": {
        "display": "A",
        "quantity": "Current",
        "quantityDisplay": "i",
        "description": "Electrical current in ampere"
      },
      "C": {
        "display": "C",
        "quantity": "Charge",
        "quantityDisplay": "Q",
        "description": "Electrical charge in Coulomb"
      },
      "V": {
        "display": "V",
        "quantity": "Voltage",
        "quantityDisplay": "V",
        "description": "Electrical potential in volt"
      },
      "W": {
        "display": "W",
        "quantity": "Power",
        "quantityDisplay": "P",
        "description": "Electrical power in watt"
      },
      "J": {
        "display": "J",
        "quantity": "Energy",
        "quantityDisplay": "E",
        "description": "Electrical energy in joule"
      },
      "ohm": {
        "display": "Ω",
        "quantity": "Resistance",
        "quantityDisplay": "R",
        "description": "Electrical resistance in ohm"
      },
      "m": {
        "display": "m",
        "quantity": "Distance",
        "quantityDisplay": "d",
        "description": "Distance in meters"
      },
      "m/s": {
        "display": "m/s",
        "quantity": "Velocity",
        "quantityDisplay": "v",
        "description": "Velocity in meters per second"
      },
      "m2": {
        "display": "㎡",
        "quantity": "Area",
        "quantityDisplay": "A",
        "description": "(Surface) area in square meters"
      },
      "K": {
        "display": "K",
        "quantity": "Temperature",
        "quantityDisplay": "t",
        "description": "Temperature in kelvin"
      },
      "Pa": {
        "display": "Pa",
        "quantity": "Pressure",
        "quantityDisplay": "P",
        "description": "Pressure in pascal"
      },
      "kg": {
        "display": "kg",
        "quantity": "Mass",
        "quantityDisplay": "m",
        "description": "Mass in kilogram"
      },
      "ratio": {
        "display": "",
        "quantity": "Ratio",
        "quantityDisplay": "φ",
        "description": "Relative value compared to reference or normal value. 0 = 0%, 1 = 100%, 1e-3 = 1 ppt"
      },
      "m/s2": {
        "display": "m/s²",
        "quantity": "Acceleration",
        "quantityDisplay": "a",
        "description": "Acceleration in meters per second squared"
      },
      "rad/s2": {
        "display": "rad/s²",
        "quantity": "Angular acceleration",
        "quantityDisplay": "a",
        "description": "Angular acceleration in radians per second squared"
      },
      "N": {
        "display": "N",
        "quantity": "Force",
        "quantityDisplay": "F",
        "description": "Force in newton"
      },
      "T": {
        "display": "T",
        "quantity": "Magnetic field",
        "quantityDisplay": "B",
        "description": "Magnetic field strength in tesla"
      },
      "Pa/s": {
        "display": "Pa/s",
        "quantity": "Pressure rate",
        "quantityDisplay": "R",
        "description": "Pressure change rate in pascal per second"
      }
    }
  },
  "mmsi": {
    "type": "string",
    "description": "Maritime Mobile Service Identity (MMSI). Has to be 9 digits. See http://en.wikipedia.org/wiki/Maritime_Mobile_Service_Identity for information.",
    "pattern": "^[2-7][0-9]{8,8}$",
    "maxLength": 9,
    "minLength": 9,
    "example": "503123456"
  },
  "uuid": {
    "type": "string",
    "description": "A unique Signal K flavoured maritime resource identifier (MRN). A MRN is a form of URN, following a specific format: urn:mrn:<issueing authority>:<id type>:<id>. In case of a Signal K uuid, that looks like this: urn:mrn:signalk:uuid:<uuid>, where Signal K is the issuing authority and UUID (v4) the ID type.",
    "pattern": "^urn:mrn:signalk:uuid:[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-4[0-9A-Fa-f]{3}-[89ABab][0-9A-Fa-f]{3}-[0-9A-Fa-f]{12}$",
    "example": "urn:mrn:signalk:uuid:b7590868-1d62-47d9-989c-32321b349fb9"
  },
  "url": {
    "type": "string",
    "description": "A location of a resource, potentially relative. For hierarchical schemes (like http), applications must resolve relative URIs (e.g. './v1/api/'). Implementations should support the following schemes: http:, https:, mailto:, tel:, and ws:.",
    "example": "http://localhost:8080/signalk/v1/api/vessels/self/environment"
  },
  "commonValueFields": {
    "type": "object",
    "required": [
      "timestamp",
      "$source"
    ],
    "properties": {
      "timestamp": {
        "$ref": "#/definitions/timestamp"
      },
      "$source": {
        "$ref": "#/definitions/sourceRef"
      },
      "_attr": {
        "$ref": "#/definitions/_attr"
      },
      "meta": {
        "$ref": "#/definitions/meta"
      },
      "pgn": {
        "type": "number"
      },
      "sentence": {
        "type": "string"
      }
    }
  },
  "numberValue": {
    "type": "object",
    "description": "Data should be of type number.",
    "allOf": [
      {
        "$ref": "#/definitions/commonValueFields"
      },
      {
        "properties": {
          "value": {
            "type": "number"
          },
          "values": {
            "type": "object",
            "patternProperties": {
              ".*": {
                "$ref": "#/definitions/valuesNumberValue"
              }
            }
          }
        }
      }
    ]
  },
  "valuesNumberValue": {
    "type": "object",
    "properties": {
      "value": {
        "type": "number"
      },
      "timestamp": {
        "$ref": "#/definitions/timestamp"
      },
      "pgn": {
        "type": "number"
      },
      "sentence": {
        "type": "string"
      }
    }
  },
  "stringValue": {
    "type": "object",
    "description": "Data should be of type number.",
    "allOf": [
      {
        "$ref": "#/definitions/commonValueFields"
      },
      {
        "properties": {
          "value": {
            "type": "string"
          },
          "values": {
            "type": "object",
            "patternProperties": {
              ".*": {
                "$ref": "#/definitions/valuesStringValue"
              }
            }
          }
        }
      }
    ]
  },
  "valuesStringValue": {
    "type": "object",
    "properties": {
      "value": {
        "type": "string"
      },
      "timestamp": {
        "$ref": "#/definitions/timestamp"
      },
      "pgn": {
        "type": "number"
      },
      "sentence": {
        "type": "string"
      }
    }
  },
  "nullValue": {
    "type": "object",
    "description": "Data should be of type NULL.",
    "properties": {
      "value": {
        "type": "null"
      },
      "timestamp": {
        "$ref": "#/definitions/timestamp"
      },
      "source": {
        "$ref": "#/definitions/source"
      },
      "_attr": {
        "$ref": "#/definitions/_attr"
      },
      "meta": {
        "$ref": "#/definitions/meta"
      }
    }
  },
  "_attr": {
    "type": "object",
    "title": "_attr schema.",
    "description": "Filesystem specific data, e.g. security, possibly more later.",
    "properties": {
      "_mode": {
        "type": "integer",
        "title": "_mode schema.",
        "description": "Unix style permissions, often written in `owner:group:other` form, `-rw-r--r--`",
        "default": 644
      },
      "_owner": {
        "type": "string",
        "title": "_owner schema.",
        "description": "The owner of this resource.",
        "default": "self"
      },
      "_group": {
        "type": "string",
        "title": "_group schema.",
        "description": "The group owning this resource.",
        "default": "self"
      }
    }
  },
  "alarmState": {
    "type": "string",
    "title": "alarmState",
    "description": "The alarm state when the value is in this zone.",
    "default": "normal",
    "enum": [
      "normal",
      "alert",
      "warn",
      "alarm",
      "emergency"
    ]
  },
  "alarmMethodEnum": {
    "enum": [
      "visual",
      "sound"
    ]
  },
  "meta": {
    "type": "object",
    "title": "Meta schema.",
    "description": "Provides meta data to enable alarm and display configuration.",
    "properties": {
      "displayName": {
        "type": "string",
        "title": "DisplayName schema.",
        "description": "A display name for this value.",
        "example": "Tachometer, Engine 1"
      },
      "longName": {
        "type": "string",
        "title": "LongName schema.",
        "description": "A long name for this value.",
        "example": "Tachometer, Engine 1"
      },
      "shortName": {
        "type": "string",
        "title": "ShortName schema.",
        "description": "A short name for this value.",
        "example": "RPM"
      },
      "gaugeType": {
        "type": "string",
        "title": "gaugeType schema.",
        "description": "The type of gauge necessary to display this value.",
        "example": "sparkline"
      },
      "units": {
        "type": "string",
        "title": "units schema.",
        "description": "The (derived) SI unit of this value.",
        "example": "m/s"
      },
      "timeout": {
        "type": "number",
        "title": "Timeout",
        "description": "The timeout in (fractional) seconds after which this data is invalid.",
        "example": 2
      },
      "alertMethod": {
        "type": "array",
        "title": "Alert Method",
        "description": "The method to use to raise the alert. An alert is an event that should be known",
        "default": [
          "visual"
        ],
        "items": {
          "$ref": "#/definitions/alarmMethodEnum"
        }
      },
      "warnMethod": {
        "type": "array",
        "title": "Warn Method",
        "description": "The method to use to raise the warning. A warning is an unexpected event that may require attention",
        "default": [
          "visual"
        ],
        "items": {
          "$ref": "#/definitions/alarmMethodEnum"
        }
      },
      "alarmMethod": {
        "type": "array",
        "title": "Alarm Method",
        "description": "The method to use to raise the alarm. An alarm requires immediate attention, eg no oil pressure",
        "default": [
          "visual",
          "sound"
        ],
        "items": {
          "$ref": "#/definitions/alarmMethodEnum"
        }
      },
      "emergencyMethod": {
        "type": "array",
        "title": "Emergency Method",
        "description": "The method to use to raise an emergency. An emergency is an immediate danger to life or vessel",
        "default": [
          "visual",
          "sound"
        ],
        "items": {
          "$ref": "#/definitions/alarmMethodEnum"
        }
      },
      "zones": {
        "type": "array",
        "title": "Zones schema.",
        "description": "The zones defining the range of values for this signalk value.",
        "items": [
          {
            "type": "object",
            "title": "zone",
            "description": "A zone used to define the display and alarm state when the value is in between bottom and top.",
            "required": [
              "state"
            ],
            "properties": {
              "lower": {
                "id": "lower",
                "type": "number",
                "title": "Lower",
                "description": "The lowest number in this zone",
                "name": "lower",
                "example": 3500
              },
              "upper": {
                "id": "upper",
                "type": "number",
                "title": "Upper",
                "description": "The highest value in this zone",
                "name": "upper",
                "example": 4000
              },
              "state": {
                "$ref": "#/definitions/alarmState"
              },
              "message": {
                "id": "message",
                "type": "string",
                "title": "message",
                "description": "The message to display for the alarm.",
                "default": "Warning"
              }
            }
          }
        ]
      }
    }
  },
  "geohash": {
    "type": "string",
    "description": "A geohash (see http://geohash.org)",
    "pattern": "^[0-9A-Za-z:]{1,}$",
    "example": "eg rbe:TasmanBay"
  },
  "position": {
    "type": "object",
    "title": "position",
    "description": "The position in 3 dimensions",
    "allOf": [
      {
        "$ref": "#/definitions/commonValueFields"
      },
      {
        "properties": {
          "longitude": {
            "type": "number",
            "description": "Longitude",
            "units": "deg",
            "example": 4.98765245
          },
          "latitude": {
            "type": "number",
            "description": "Latitude",
            "units": "deg",
            "example": 52.0987654
          },
          "altitude": {
            "type": "number",
            "description": "Altitude",
            "units": "m"
          }
        }
      }
    ]
  },
  "waypoint": {
    "type": "object",
    "description": "A waypoint, an object with a signal k position object, and GeoJSON Feature object (see geojson.org, and https://github.com/fge/sample-json-schemas/tree/master/geojson)",
    "properties": {
      "position": {
        "$ref": "#/definitions/position"
      },
      "feature": {
        "title": "Feature",
        "description": "A Geo JSON feature object",
        "required": [
          "geometry",
          "properties"
        ],
        "properties": {
          "type": {
            "enum": [
              "Feature"
            ]
          },
          "geometry": {
            "title": "Point",
            "properties": {
              "type": {
                "enum": [
                  "Point"
                ]
              },
              "coordinates": {
                "description": "A single position, in x,y order (Lon, Lat)",
                "type": "array",
                "minItems": 2,
                "items": [
                  {
                    "type": "number"
                  },
                  {
                    "type": "number"
                  }
                ],
                "additionalItems": false
              }
            }
          },
          "properties": {
            "type": [
              "object",
              "null"
            ],
            "description": "Additional data of any type",
            "additionalProperties": true
          },
          "id": {
            "FIXME": "may be there, type not known (string? number?)"
          }
        }
      }
    }
  }
}
```

---