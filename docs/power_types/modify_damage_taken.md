---
title: Modify Damage Taken (Power Type)
date: 2021-04-06
---
# Modify Damage Taken

[Power Type](../power_types.md).

Modifies how much damage the player takes.

Type ID: `origins:modify_damage_taken`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If set, the modifiers will only apply to damage which satisfies this condition.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If set, this modifier will apply to the damage amount.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, these modifiers will apply to the damage amount.
`self_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player whenever this power applies a modification.
`attacker_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the attacker whenever this power applies a modification.


### Example
```json
{
    "type": "origins:modify_damage_taken",
    "damage_condition": {
        "type": "origins:attacker",
        "entity_condition": {
            "type": "origins:equipped_item",
            "equipment_slot": "mainhand",
            "item_condition": {
                "type": "origins:or",
                "conditions": [
                    {
                        "type": "origins:enchantment",
                        "enchantment": "minecraft:binding_curse",
                        "comparison": ">=",
                        "compare_to": 1
                    },
                    {
                        "type": "origins:enchantment",
                        "enchantment": "minecraft:vanishing_curse",
                        "comparison": ">=",
                        "compare_to": 1
                    }
                ]
            }
        }
    },
    "modifier": {
        "name": "Weak to cursed items",
        "operation": "addition",
        "value": 5.5
    }
}
```
This power will make the player take 3 hearts of damage if the attacker is holding an item with either the Curse of Binding, or Curse of Vanishing enchantments.