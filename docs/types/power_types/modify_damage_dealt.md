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
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If specified, the specified modifier(s) and/or action(s) will only apply if the dealt damage fulfills this condition.
`modifier` | [Attribute Modifier](../types/data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the damage amount.
`modifiers` | [Array](../types/data_types/array.md) of [Attribute Modifiers](../types/data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the damage amount.
`target_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If specified, the specified modifier(s) and action(s) will only be applied if the entity/entities that has been hit fulfills this condition.
`self_action` | [Entity Action](../entity_actions.md) | _optional_ | If specified, this action will be executed on the entity that has the power whenever the modifier(s) is applied.
`target_action` | [Entity Action](../entity_actions.md) | _optional_ | If specified, this action will be executed on the entity/entities that has been hit whenever the modifier(s) is applied.


### Example
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
This example gives the player additional 2 and a half hearts of damage if the player is inside a water fluid, regardless of its fluid level.