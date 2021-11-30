---
title: Modify Damage Dealt (Power Type)
date: 2021-04-06
---

# Modify Damage Dealt

[Power Type](../power_types.md)

Modifies how much melee damage the entity that has the power deals.

Type ID: `origins:modify_damage_dealt`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the specified modifier(s) and/or action(s) will only apply if the dealt damage fulfills this condition.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the damage amount.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the damage amount.
`target_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, the specified modifier(s) and action(s) will only be applied if the entity/entities that has been hit fulfills this condition.
`self_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity that has the power whenever the modifier(s) is applied.
`target_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity/entities that has been hit whenever the modifier(s) is applied.



### Examples

```json
{
    "type": "origins:modify_damage_dealt",
    "condition": {
        "type": "origins:in_block_anywhere",
        "block_condition": {
            "type": "origins:block",
            "block": "minecraft:water"
        },
        "comparison": ">=",
        "compare_to": 1
    },
    "modifier": {
        "name": "Extra damage when submerged",
        "operation": "addition",
        "value": 5.0
    }
}
```

This example will give the entity that has the power additional 2 and a half hearts of damage if the entity is in Water, regardless of its fluid level.
