---
title: Action on Set (Entity Action Type)
date: 2023-12-14
---


#	Action on Set

[Entity Action Type](../entity_action_types.md)

Executes an action on entities stored within the power that uses the [Entity Set (Power Type)](../power_types/entity_set.md).

Type ID: `origins:action_on_set`


!!!	note

	In the context of this entity action type, the actor will be the entity that invoked the entity action while the target will be the entities within the power.

!!!	note

	The action will be executed on the entities stored within the power regardless of their dimension.


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`set` | [Identifier](../data_types/identifier.md) | | The ID of the power.
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | | The bi-entity action to execute on both or either the actor and target.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | *optional* | If specified, only execute the bi-entity action if this bi-entity condition is fulfilled by both or either the actor and target.
`limit` | [Integer](../data_types/integer.md) | `0` | Determines the max amount of times the entity action type should iterate and execute the bi-entity action on the entities stored within the power. If the value is less than or equal to `0`, then there will be no limit.
`reverse` | [Boolean](../data_types/boolean.md) | `false` | Determines whether to reverse the order of the entities within the power when processing.


###	Examples

```json
"entity_action": {
	"type": "origins:action_on_set",
	"set": "example:special_pets",
	"bientity_action": {
		"type": "origins:heal",
		"amount": 4
	}
}
```

This example will restore 2 hearts to entities that were added to the `example:special_pets` (`data/example/powers/special_pets.json`) power using the [Add to Set (Bi-entity Action Type)](../bientity_action_types/add_to_set.md).
