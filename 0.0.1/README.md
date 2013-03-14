# BuildingJSON 0.0.1

A metadata model for building information.

## 1. Purpose

This specification attempts to create a standard for representing metadata about multiple types of building & building information.

## 2. File format

BuildingJSON manifest files use the JSON format as described in RFC 4627.

```javascript
{
	// A semver.org style version number. Describes the version of
	// the BuildingJSON spec that is implemented by this JSON object.
	"buildingjson": "0.0.1",

	// A name describing the building.
	"name": "String",

	// A short or nickname.
	"nickname": "String",

	// Building description.
	"description": "String",

	// Description containing parking opportunities.
	"description_parking": "String",

	// Building accessibility description.
	"description_barrier_free": "String",
	
	// Buildings street (Address).
	"street": "String",

	// Buildings house number (Address).
	"house_number": "String",

	// Buildings zip (Address).
	"zip": "Number",

	// Buildings city (Address).
	"city": "String",

	// Buildings province (Address).
	"province": "String",

	// Buildings lat/lon (Address).
	"lat": "Number",
	"lon": "Number",

	// Building floors.
	"floors": [
		{
			// Floor name.
			"name": "String",

			// A short or nickname.
			"nickname": "String"

			// Floor rooms.
			"rooms": {
				"room-name": "String",
				"room-number": "String|Number",
				"usage": "String",
				"size": "Number"
			}
		}
	]
}
```