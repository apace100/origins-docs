---
title: Type (Damage Condition Type)
date: 2023-10-26
---


#	Type

[Damage Condition Type](../damage_condition_types.md)

Checks whether the damage source is of a certain damage type.

Type ID: `origins:type`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`damage_type` | [Identifier](../data_types/identifier.md) | | The ID of the damage type to compare the damage source to.


###	Examples

```json
"damage_condition": {
	"type": "origins:type",
	"damage_type": "minecraft:magic"
}
```

This example will check if the damage source is of the `minecraft:magic` damage type.
