---
title: Game Event Listener (Power Type)
date: 2023-10-09
---

# Game Event Listener

[Power Type](../power_types.md)

Executes an action upon listening to a game event or vibration.

Type ID: `origins:game_event_listener`

!!! note

    In the context of this power type, the '**actor**' entity is the entity that emmited the game event or vibration while the '**target**' entity is the entity that has the power.

!!! note

    See [Minecraft Wiki: Sculk Sensor (Vibration amplitudes)](https://minecraft.wiki/w/Sculk_Sensor?oldid=2099339#Vibration_amplitudes) for a list of vanilla game events you can check for.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either or both the '**actor**' and '**target**' entities.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`block_action` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this block action type will be executed at the position where the game event or vibration was emitted.
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, only executes the actions if the game event or vibration is emitted by a block that fulfills the block condition.
`cooldown` | [Integer](../data_types/integer.md) | `1` | Interval of ticks this power needs to recharge before being able to listen to game events or vibrations again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.
`event` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, will make the power only listen for the game events with this namespace and IDs.
`events` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, will make the power only listen for the game events with these namespace and IDs.
`event_tag` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, will make the power only listen for the game events inside game event tag.
`show_particle` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the vibration should emit a particle effect.


### Examples

```json
{
    "type": "origins:game_event_listener",
    "bientity_action": {
        "type": "origins:target_action",
        "action": {
            "type": "origins:set_on_fire",
            "duration": 5
        }
    },
    "event": "minecraft:hit_ground"
}
```

This example will set the entity with the power on fire every time the `hit_ground` game event is emmited.
