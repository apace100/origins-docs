---
title: Modify Inventory (Entity Action Type)
date: 2022-06-07
---

#   Modify Inventory

[Entity Action Type](../entity_action_types.md)

Modifies the items from either the entity's inventory or a power that uses the [Inventory (Power Type)](../power_types/inventory.md).

Type ID: `origins:modify_inventory`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`inventory_type` | [Inventory Type](../../misc/extras/inventory_type.md) | `"inventory"` | Determines whether to modify the items in the inventory of the entity or the inventory of a power present in the entity.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity **before** the items are modified.
`item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the affected items.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, only items which fulfill this condition will be affected by specified action.
`slot` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, only items in the designated slot will be modified. See [Positioned Item Stack Slots](../../misc/extras/positioned_item_stack_slots.md) for possible values.
`slots` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | See [Positioned Item Stack Slots](../../misc/extras/positioned_item_stack_slots.md) for possible values.
`power` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the items in the inventory of this power will be modified instead of the items in the entity's inventory if `inventory_type` is set to `"power"`.


### Examples

```json
"entity_action": {
    "type": "origins:modify_inventory",
    "inventory_type": "power",
    "power": "origins:extra_inventory",
    "item_action": {
        "type": "origins:consume"
    }
}
```

This example will consume each item in the inventory of the `origins:extra_inventory` power, decreasing their count by 1.
<br>

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
