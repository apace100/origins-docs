---
title: Modify Projectile Dealt (Power Type)
date: 2021-04-08
---

# Modify Projectile Damage

[Power Type](../power_types.md)

Modifies how much damage the projectile of the entity that has the power deals.

Type ID: `origins:modify_projectile_damage`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If specified, the specified modifier(s) and action(s) will only apply if the dealt damage fulfills by this condition.
`modifier` | [Attribute Modifier](../types/data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the damage amount.
`modifiers` | [Array](../types/data_types/array.md) of [Attribute Modifiers](../types/data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the damage amount.
`target_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If specified, the specified modifier(s) and action(s) will only apply if the the entity that has been hit fulfills this condition.
`self_action` | [Entity Action](../entity_actions.md) | _optional_ | If specified, this action will be executed on the 'actor' entity (the entity that has the power) whenever the modifier(s) are applied.
`target_action` | [Entity Action](../entity_actions.md) | _optional_ | If specified, this action will be executed on the the entity that has been hit whenever the modifier(s) are applied.


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
