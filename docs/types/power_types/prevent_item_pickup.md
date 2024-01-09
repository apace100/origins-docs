---
title: Prevent Item Pickup (Power Type)
date: 2024-01-10
---


#	Prevent Item Pickup

[Power Type](../power_types.md)

Prevents the entity that has the power from picking up an item.

Type ID: `origins:prevent_item_pickup`


!!!	note

	The actor and target context of certain fields of this power type are as follows:

	Field | Actor | Target
	------|-------|-------
	`bientity_action_thrower` | The entity that threw the item. | The entity about to pick up the item.
	`bientity_action_item` | The entity about to pick up the item. | The item entity to be picked up.
	`bientity_condition` | The entity that threw the item. | The entity about to pick up the item.


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action_thrower` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | If specified, this bi-entity action will be executed on either or both the actor and target entities (See to the table above to determine which actor/target entity is being referred to.)
`bientity_action_item` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | If specified, this bi-entity action will be executed on either or both the actor and target entities (See to the table above to determine which actor/target entity is being referred to.)
`item_action` | [Item Action Type](../item_action_types.md) | *optional* | If specified,this item action will be executed on the item that was attempted to be picked up.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | *optional* | If specified, the restriction will only happen if this bi-entity condition is fulfilled by either or both the actor and target entities (See the table above to determine which actor/target entity is being referred to.)
`item_condition` | [Item Condition Type](../item_condition_types.md) | *optional* | If specified, the restriction will only happen if this item condition is fulfilled by the item about to be picked up.
`priority` | [Integer](../data_types/integer.md) | `0` | Determines the execution priority of the powers that use this power type (in a low-to-high priority order.)


###	Examples

```json
{
	"type": "origins:prevent_item_pickup",
	"item_condition": {
		"type": "origins:meat"
	}
}
```

This example will prevent the entity that has the power from picking up food items that are considered meat.
