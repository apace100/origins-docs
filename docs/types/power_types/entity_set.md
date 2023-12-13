---
title: Entity Set (Power Type)
date: 2023-12-13
---


#	Entity Set

[Power Type](../power_types.md)

Provides a "set" (a storage) for storing entities that can be used for executing actions on the entities within the set, or checking whether an entity is stored within the set.

Type ID: `origins:entity_set`


!!!	note

	In the context of this power type, the '**actor**' will be the entity that has the power while the '**target**' will be the entities within the set.

!!!	note

	Entities are not stored in the set physically, meaning that the entity will continue to exist as is. The UUID of the entity is stored in the power's data, allowing for the power type to access the entity for later use (unless the entity no longer exists).


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`action_on_add` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | If specified, this bi-entity action will be executed on either or both the '**actor**' and the '**target**' upon the '**target**' being added to the set.
`action_on_remove` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | If specified, this bi-entity action will be executed on either or both the '**actor**' and the '**target**' upon the '**target**' being removed from the set.


###	Examples

```json
{
	"type": "origins:entity_set"
}
```

This example simply provides a set. No actions will be executed to entities being added to or removed from the set.
<br>


```json
{
	"type": "origins:entity_set",
	"action_on_remove": {
		"type": "origins:damage",
		"damage_type": "minecraft:generic",
		"amount": 6
	}
}
```

This example will deal 6 (3 hearts of) damage to entities that were removed from the set. 
