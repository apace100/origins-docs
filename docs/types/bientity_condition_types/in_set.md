---
title: In Set (Bi-entity Condition Type)
date: 2023-12-14
---


#	In Set

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks whether the target entity is within a power that uses the [Entity Set (Power Type)](../power_types/entity_set.md) of the actor entity.

Type ID: `origins:in_set`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`set` | [Identifier](../data_types/identifier.md) | | The ID of the power to check whether the target entity is in.


###	Examples

```json
"bientity_condition": {
	"type": "origins:or",
	"conditions": [
		{
			"type": "origins:owner"
		},
		{
			"type": "origins:in_set",
			"set": "example:special_pets"
		}
	]
}
```

This example will check whether the target entity is either owned by the actor entity or if the target entity is within the `example:special_pets` (`data/example/powers/special_pets.json`) power.
