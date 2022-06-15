---
title: Replace Inventory (Entity Action Type)
date: 2022-06-15
---

#   Replace Inventory

[Entity Action Type](../entity_action_types.md)

Replaces the items from either the entity's inventory or a power that uses the [Inventory (Power Type)](../power_types/inventory.md).

Type ID: `origins:replace_inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`inventory_type` | [Inventory Type](../../misc/extras/inventory_type.md) | `"inventory"` | Determines whether to replace the items from the inventory of the entity or the inventory of a power present in the entity.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity **before** the items are replaced.
`item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the affected items **after** the affected items are replaced.
`item_condition` | [Item Condition Type](../item_condition_types/amount.md) | _optional_ | If specified, only items which fulfill this condition will be replaced.
`slot` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, only items in the designated slot will be replaced. All valid inputs can be found [here](https://minecraft.fandom.com/wiki/Slot#Command_argument).
`slots` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, only items in the designated slots will be dropped. All valid inputs can be found [here](https://minecraft.fandom.com/wiki/Slot#Command_argument)
`power` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the items in the inventory of this power will be replaced instead of the items in the entity's inventory if `inventory_type` is set to `"power"`.
`stack` | [Item Stack](../data_types/item_stack.md) | | The item to use as a replacement for the affected items.


### Examples

```json
"entity_action": {
    "type": "origins:replace_inventory",
    "slot": "weapon.offhand",
    "stack": {
        "item": "minecraft:barrier"
    }
}
```

This example will replace the item in the entity's offhand with a Barrier item.
<br>

```json
"entity_action": {
    "type": "origins:replace_inventory",
    "inventory_type": "power",
    "power": "origins:extra_inventory",
    "stack": {
        "item": "minecraft:air"
    }
}
```

This example will clear the contents of the `origins:extra_inventory` power by replacing all the items with Air.
