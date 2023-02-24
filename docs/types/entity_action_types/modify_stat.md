---
title: Modify Stat (Entity Action Type)
date: 2022-07-03
---

#   Modify Stat

[Entity Action Type](../entity_action_types.md)

Modifies the value of a certain statistic with [Attribute Modifiers](../data_types/attribute_modifier.md).

Type ID: `origins:modify_stat`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`stat` | [Stat](../data_types/stat.md) | | The type and name of the statistic to be modified.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | | This modifier will be applied to the current value of the statistic specified.


### Examples

```json
"entity_action": {
    "type": "origins:modify_stat",
    "stat": {
        "type": "minecraft:custom",
        "id": "minecraft:time_since_rest"
    },
    "modifier": {
        "operation": "add_base_early",
        "value": 24000
    }
}
```

This example will add 24000 to the value of the player's `minecraft.custom:minecraft.time_since_rest` statistic.
<br>

```json
"entity_action": {
    "type": "origins:modify_stat",
    "stat": {
        "type": "minecraft:used",
        "id": "origins:orb_of_origin"
    },
    "modifier": {
        "operation": "add_base_early",
        "value": 1
    }
}
```

This example will add 1 to the value of the player's `minecraft.used:origins.orb_of_origin` statistic.
