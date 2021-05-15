---
title: Modify Damage Dealt (Power Type)
date: 2021-04-06
---
# Modify Damage Dealt

[Power Type](../power_types.md).

Modifies how much melee damage the player deals.

Type ID: `origins:modify_damage_dealt`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If set, the modifiers will only apply to damage which satisfies this condition.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If set, this modifier will apply to the damage amount.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, these modifiers will apply to the damage amount.
`target_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If set, the action will only be triggered when a target matching this condition is hit.
`self_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player whenever this power applies a modification.
`target_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the target whenever this power applies a modification.


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