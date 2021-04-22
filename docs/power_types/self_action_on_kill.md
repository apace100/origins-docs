---
title: Self Action On Kill (Power Type)
date: 2021-04-04
---
# Self Action On Kill

[Power Type](../power_types.md).

Executes an entity action on the player when the player kills another entity.

Type ID: `origins:self_action_on_kill`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | | The action to execute on the player.
`cooldown` | [Integer](../data_types/integer.md) | | Interval of ticks this power needs to recharge before the action can be executed again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | If set, the cooldown of this power is visualized on the HUD in the specified way.
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If set, the action will only trigger when this condition holds for the damage that was dealt by the player.
`target_condition` | [Target Condition](../entity_conditions.md) | _optional_ | If set, the action will only be triggered when a target matching this condition is killed.


### Example
```json
{
    "type": "origins:self_action_on_kill",
    "entity_action": {
        "type": "origins:heal",
        "amount": 4.0
    },
    "cooldown": 100,
    "hud_render": {
        "should_render": true,
        "sprite_location": "origins:textures/gui/community/spiderkolo/resource_bar_01.png",
        "bar_index": 5
    },
    "damage_condition": {
        "type": "origins:attacker",
        "entity_condition": {
            "type": "origins:equipped_item",
            "equipment_slot": "mainhand",
            "item_condition": {
                "type": "origins:ingredient",
                "ingredient": {
                    "item": "minecraft:iron_sword"
                }
            }
        }
    }
}
```
This power will heal the player if the player has killed a mob with an iron sword.