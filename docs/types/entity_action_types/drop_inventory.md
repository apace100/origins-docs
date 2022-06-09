---
title: Drop Inventory (Entity Action Type)
date: 2022-6-07
---

# Drop Inventory

[Entity Action Type](../entity_action_types.md)

Drops items from either the entity's inventory or a power that uses the [Inventory (Power Type)](../../power_types/inventory.md).

Type ID: `origins:drop_inventory`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`inventory_type` | [Identifier](../../data_types/identifier.md) | `inventory` | Takes one of either `inventory` or `power`. Determines whether you're dropping items from the player inventory, or the extra inventory from the [`origins:inventory`](../types/power_types/inventory.md) power type respectively.
`entity_action` | [Entity Action](../types/entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity **before** the items are dropped.
`item_action` | [Item Action](../types/item_action_types.md) | _optional_ | If specified, this action will be executed on the affected items **before** they are dropped.
`item_condition` | [Item Condition](../types/item_condition_types.md) | _optional_ | If specified, only items which fulfill this condition will be dropped.
`slot` | [Identifier](../../data_types/identifier.md) | _optional_ | If specified, only items in the designated slot will be dropped. All valid inputs can be found [here](https://minecraft.fandom.com/wiki/Slot#Command_argument)
`slots` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, only items in the designated slots will be dropped. All valid inputs can be found [here](https://minecraft.fandom.com/wiki/Slot#Command_argument)
`power` | [Identifier](../data_types/identifier.md) | _optional_ | Used to specify which power will be affected if the `inventory_type` field is set to `power`.
`throw_randomly` | [Boolean](../data_types/boolean.md) | `false` | If true, items will be thrown in random directions instead of being normally dropped, similar to how items are dropped when you die.
`retain_ownership` | [Boolean](../data_types/boolean.md) | `true` | If true, dropped items will have their `Owner` tag match the UUID of the player who the item originally belonged to, preventing others from picking it up before the original owner has a chance. 


### Examples

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
