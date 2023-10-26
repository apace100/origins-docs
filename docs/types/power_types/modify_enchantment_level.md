---
title: Modify Enchantment Level (Power Type)
date: 2023-10-09
---

# Modify Enchantment Level

[Power Type](../power_types.md)

Applies/modifies the level of the specified enchantment to/from the entity.

Type ID: `origins:modify_enchantment_level`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`enchantment` | [Identifier](../data_types/identifier.md) |  | ID of the enchantment to apply/modify the level of to the entity., e.g. `minecraft:protection`.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, only applies/modifies the level of the specified enchantment to/from the entity if the item condition is fulfilled by the item.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the current level of the specified enchantment from the entity.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the current level of the specified enchantment from the entity.


### Examples

```json
{
    "type": "origins:modify_enchantment_level",
    "enchantment": "minecraft:silk_touch",
    "modifier": {
        "operation": "set_total",
        "value": 1
    }
}
```

This example will grant the player the ability to use Silk Touch, regardless of whether the player is holding any item or no item at all.
