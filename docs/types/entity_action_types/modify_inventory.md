---
title: Modify Inventory (Entity Action Type)
date: 2022-6-07
---

# Modify Inventory

[Entity Action Type](../entity_action_types.md)

Selects items from anywhere in a player's inventory to modify them with an [Item Action](../types/item_action_types.md).

Type ID: `origins:modify_inventory`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`inventory_type` | [Identifier](../../data_types/identifier.md) | `inventory` | Takes one of either `inventory` or `power`. Determines whether you're modified items from the player inventory, or the extra inventory from the [`origins:inventory`](../types/power_types/inventory.md) power type respectively.
`entity_action` | [Entity Action](../types/entity_action_types.md) | _optional_ | If specified, this action will be ran after the items are modified.
`item_action` | [Item Action](../types/item_action_types.md) | _optional_ | If specified, this action will be ran on all specified items.
`item_condition` | [Item Condition](../types/item_condition_types.md) | _optional_ | If specified, only items which fulfill this condition will be affected by item actions.
`slot` | [Identifier](../../data_types/identifier.md) | _optional_ | If specified, only items in the designated slot will be modified. All valid inputs can be found [here](https://minecraft.fandom.com/wiki/Slot#Command_argument)
`slots` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, only items in the designated slots will be modified. All valid inputs can be found [here](https://minecraft.fandom.com/wiki/Slot#Command_argument)
`power` | [Identifier](../data_types/identifier.md) | _optional_ | Used to specify which power will be affected if the `inventory_type` field is set to `power`.


### Examples

```json
"entity_action": {
	"type": "origins:modify_inventory",
  "item_condition": {
		"type": "origins:armor_value",
		"comparison": ">",
		"compare_to": 0
	},
	"item_action": {
		"type": "origins:damage",
		"amount": 1,
		"ignore_unbreaking": true
	}
}
```

This example will slightly damage all items with an armor value.
