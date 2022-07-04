---
title: Modify Damage Dealt (Power Type)
date: 2021-04-06
---

# Modify Damage Dealt

[Power Type](../power_types.md)

Modifies how much melee damage the entity that has the power deals.

Type ID: `origins:modify_damage_dealt`

!!! note

    In the context of this power type, the '**actor**' entity is the entity that has the power whilst the '**target**' entity is the entity that was hit.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either or both the '**actor**' and '**target**' entities whenever the modifier(s) is/are applied.
`self_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the '**actor**' entity whenever the modifier(s) is/are applied.
`target_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the '**target**' entity whenever the modifier(s) is/are applied.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified action(s)/modifier(s) will only be executed/applied if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`target_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, the specified actions/modifiers will only be executed/applied if this condition is fulfilled by the '**target**' entity.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the specified actions/modifiers will only be executed/applied if this condition is fulfilled by the damage dealt by the '**actor**' entity.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the damage dealt by the '**actor**' entity.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied t othe damage dealt by the '**actor**' entity.


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
