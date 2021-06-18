---
title: Array (Data Type)
date: 2021-04-04
---
# Array

[Data Type](../data_types.md).

Arrays are lists of other existing data types. They are enclosed by square brackets and each element is separated from the next by a comma.

### Examples:

```json
{
	"field_name": [
		"first_value",
		"second_value",
		"third"
	]
}
```

An array of [Strings](string.md).
<br>


```json
{
	"type": "origins:or",
	"conditions": [
		{
			"type": "origins:on_fire"
		},
		{
			"type": "origins:sprinting"
		}
	]
}
```

An array of [Entity Conditions](../entity_conditions.md) that uses the [`origins:or` meta condition type](../meta_conditions/or.md).