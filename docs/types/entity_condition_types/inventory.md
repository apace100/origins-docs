---
title: Inventory (Entity Condition Type)
date: 2023-07-16
---

#   Inventory

Entity Condition Type

Checks if the inventory of the entity is occupied.

Type ID: `origins:inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`inventory_types` | [Array](../data_types/array.md) of [Inventory Types](../data_types/inventory_type.md) | `["inventory"]` | Determines whether to check for items in the entity's inventory, inventories of powers present in the entity, or both.
`process_mode` | [Process Mode](../data_types/process_mode.md) | `"items"` | Determines how the item stacks in the specified inventory/inventories are evaluated.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, only account for items from the specified inventory/inventories that fulfill this condition.
`slots` | [Array](../data_types/array.md) of [Item Slots](../data_types/item_slot.md) | _optional_ | If specified, only items from these specified item slots are evaluated.
`slot` | [Item Slot](../data_types/item_slot.md) | _optional_ | If specified, only the item from this specified item slot is evaluated.
`power` | [Identifier](../data_types/identifier.md) | _optional_ | If specified and if `inventory_type` is `"power"`, the items in the inventory of this power will be evaluated instead.
`comparison` | [Comparison](../data_types/comparison.md) | `">"` | Determines how the amount of items/stacks that were evaluated should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `0` | The value at which the amount of items/stacks that were evaluated will be compared to.


### Examples

```json
"condition": {
    "type": "origins:inventory",
    "process_mode": "stacks",
    "comparison": ">=",
    "compare_to": 10
}
```

This example will check if 10 or more slots are occupied by any items in the entity's inventory.
<br>

```json
"condition": {
    "type": "origins:inventory",
    "process_mode": "items",
    "item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "tag": "minecraft:flowers"
        }
    },
    "comparison": "<",
    "compare_to": 16
}
```

This example will check if 15 or less individual items that are included in the `#minecraft:flowers` (`data/minecraft/tags/items/flowers.json`) item tag are in the inventory of the entity.
