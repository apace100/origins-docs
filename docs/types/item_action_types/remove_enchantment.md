---
title: Remove Enchantment (Item Action Type)
date: 2022-07-03
---

#   Remove Enchantment

[Item Action Type](../item_action_types.md)

Removes certain enchantments from the item.

Type ID: `origins:remove_enchantment`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`enchantment` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, this enchantment will be removed from the item.
`enchantments` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, these enchantments will be removed from the item.
`levels` | [Integer](../data_types/integer.md) | _optional_ | If specified, only the enchantments that has the specified level will be removed from the item.
`reset_repair_cost` | [Boolean](../data_types/boolean.md) | `false` | Determines whether the 'repair cost' of the item should be reset.


### Examples

```json
"item_action": {
    "type": "origins:remove_enchantment",
    "enchantment": "minecraft:mending",
    "reset_repair_cost": true
}
```

This example will remove the Mending enchantment from the item whilst resetting its 'repair cost'.
