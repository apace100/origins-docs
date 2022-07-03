---
title: Modify Stat (Entity Action Type)
date: 2022-07-03
---

#   Modify Stat

[Entity Action Type](../entity_action_types.md)

Modifies the value of a certain statistic with [Attribute Modifiers](../data_types/attribute_modifier.md).

Type ID: `origins:modify_stat`

!!! note

    Refer to [Minecraft Fandom Wiki: Statistics (Resource location)](https://minecraft.fandom.com/wiki/Statistics#Resource_location) for a list of **vanilla** statistics you can modify.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`stat` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the statistic to be modified.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier_operation.md) | | This modifier will be applied to the current value of the statistic specified.


### Examples

```json
"entity_action": {
    "type": "origins:modify_stat",
    "stat": "minecraft.custom:minecraft.time_since_rest",
    "modifier": {
        "operation": "add_base_early",
        "value": 24000
    }
}
```

This example will add 24000 to the value of the player's `minecraft.custom:minecraft.time_since_rest` statistic.
