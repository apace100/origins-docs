---
title: Modify Projectile Dealt (Power Type)
date: 2021-04-08
---
# Modify Projectile Dealt

[Power Type](../power_types.md).

Modifies how much projectile damage the player deals.

Type ID: `origins:modify_projectile_damage`

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
    "type": "origins:modify_projectile_damage",
    "damage_condition": {
        "type": "origins:projectile",
        "projectile": "minecraft:spectral_arrow"
    },
    "modifier": {
        "operation": "addition",
        "value": 8.0
    }
}
```
This power modifies the damage of the spectral arrow projectile shot by the player to deal 7 and a half hearts of damage.