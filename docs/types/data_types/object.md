---
title: Object (Data Type)
date: 2021-04-04
---

# Object:

[Data Type](../data_types.md)

A complex piece of data consisting of more fields. Objects are enclosed in curly braces and contain multiple `"key": value` entries separated by commas.


### Examples

```json
{
	"field_name": {
		"field_1": "value_1",
		"field_2": 3,
		"field_3": [
			"array_value_1",
			"array_value_2"
		]
	}
}
```
An object containing a [String](string.md) field, an [Integer](integer.md) field, and an [Array](array.md) of [Strings](string.md).
<br>

```json
"effect": {
    "effect": "minecraft:slowness",
    "amplifier": 1,
    "duration": 80
}
```

An object in the format of a [Status Effect Instance](status_effect_instance.md), specifying a Slowness II status which lasts for 4 seconds.