---
title: Modify Damage Dealt (Power Type)
date: 2021-04-06
---

# Modify Damage Dealt

[Power Type](../power_types.md)

Modifies how much melee damage the entity that has the power deals.

For the `bientity_action` and `bientity_condition`, the actor is the entity that attacks (left-clicks and has the power) the target entity.

Type ID: `origins:modify_damage_dealt`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified modifier(s) and/or action(s) will only apply if either or both 'actor' (the entity that has the power) and 'target' (the entity that has been hit) fulfills this bi-entity condition type.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the specified modifier(s) and/or action(s) will only apply if the dealt damage fulfills this condition.
`target_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, the specified modifier(s) and action(s) will only be applied if the entity/entities that has been hit fulfills this condition.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the damage amount.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the damage amount.
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this bi-entity action type will be executed on either or both 'actor' (the entity that has the power) and 'target' (the entity that has been hit).
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
<br>

```json
{
    "type": "origins:modify_damage_dealt",
    "bientity_condition": {
        "type": "origins:owner"
    },
    "modifier": {
        "operation": "multiply_total",
        "value": -1
    }
}
```

This example will nullify the damage dealt to an entity if that entity is owned by the entity that has the power. (Essentially, dealing no damage to one's pets and such.)
