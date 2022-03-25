---
title: Self Action On Kill (Power Type)
date: 2021-04-04
---

# Self Action On Kill

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) on the entity that has the power when the entity kills another entity.

Type ID: `apoli:self_action_on_kill`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | | The action to execute on the entity.
`cooldown` | [Integer](../data_types/integer.md) | | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | If specified, determines how the cooldown of this power is visualized on the HUD.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the specified action will only execute if the damage dealt by the entity fulfills this condition.
`target_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, the specified action will only execute if the entity that has been killed fulfills this condition.



### Examples

```json
{
    "type": "apoli:self_action_on_kill",
    "entity_action": {
        "type": "apoli:heal",
        "amount": 4.0
    },
    "cooldown": 100,
    "hud_render": {
        "should_render": true,
        "sprite_location": "apoli:textures/gui/community/spiderkolo/resource_bar_01.png",
        "bar_index": 5
    },
    "condition": {
        "type": "apoli:equipped_item",
        "equipment_slot": "mainhand",
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "item": "minecraft:iron_sword"
            }
        }
    }
}
```

This example will restore 2 hearts to the entity that has the power if the entity has killed a mob with an Iron Sword.
