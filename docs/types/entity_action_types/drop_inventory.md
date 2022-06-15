---
title: Drop Inventory (Entity Action Type)
date: 2022-06-07
---

#   Drop Inventory

[Entity Action Type](../entity_action_types.md)

Drops the items from either the entity's inventory or a power that uses the [Inventory (Power Type)](../power_types/inventory.md).

Type ID: `origins:drop_inventory`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`inventory_type` | [Inventory Type](../../misc/extras/inventory_type.md) | `"inventory"` | Determines whether to drop the items from the inventory of the entity or the inventory of a power present in the entity.
`entity_action` | [Entity Action Type](../types/entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity **before** the items are dropped.
`item_action` | [Item Action Type](../types/item_action_types.md) | _optional_ | If specified, this action will be executed on the affected items **before** the affected items are dropped.
`item_condition` | [Item Condition Type](../types/item_condition_types.md) | _optional_ | If specified, only items which fulfill this condition will be dropped.
`slot` | [Identifier](../../data_types/identifier.md) | _optional_ | If specified, only items in the designated slot will be dropped. All valid inputs can be found [here](https://minecraft.fandom.com/wiki/Slot#Command_argument)
`slots` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, only items in the designated slots will be dropped. All valid inputs can be found [here](https://minecraft.fandom.com/wiki/Slot#Command_argument)
`power` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the items in the inventory of this power will be dropped instead of the items in the entity's inventory if `inventory_type` is set to `"power"`.
`throw_randomly` | [Boolean](../data_types/boolean.md) | `false` | If `true`, items will be thrown in random directions instead of being normally dropped, similar to how items are dropped when you die.
`retain_ownership` | [Boolean](../data_types/boolean.md) | `true` | If `true`, the dropped items will have their `Thrower` NBT set as the `UUID` NBT of the entity that invoked the action.


### Examples

```json
"entity_action": {
    "type": "origins:drop_inventory"
}
```

This example will drop all the items from the entity's inventory.
<br>

```json
"entity_action": {
	"type": "origins:drop_inventory",
	"slots": [
		"weapon.offhand",
		"hotbar.0",
		"hotbar.1",
		"hotbar.2",
		"hotbar.3",
		"hotbar.4",
		"hotbar.5",
		"hotbar.6",
		"hotbar.7",
		"hotbar.8"
	]
}
```

This example will drop all items located in your offhand, or hotbar.
