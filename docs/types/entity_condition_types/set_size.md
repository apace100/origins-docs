---
title: Set Size (Entity Condition Type)
date: 2023-12-14
---


#	Set Size

[Entity Condition Type](../entity_condition_types.md)

Compares the amount of entities stored in a power that uses the [Entity Set (Power Type)](../power_types/entity_set.md) to a certain value.

Type ID: `origins:set_size`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`set` | [Identifier](../data_types/identifier.md) | | The ID of the power.
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the amount of referenced entities in the specified power should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value at which the amount of referenced entities in the specified power will be compared to.


###	Examples

```json
"condition": {
	"type": "origins:set_size",
	"set": "example:special_pets",
	"comparison": ">",
	"compare_to": 0
}
```

This example will check if the amount of entities stored in the `example:special_pets` (`data/example/powers/special_pets.json`) power is non-zero (e.g: if it's not empty).
