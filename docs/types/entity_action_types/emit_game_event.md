---
title: Emit Game Event (Entity Action Type)
date: 2021-10-03
---

# Emit Game Event

[Entity Action Type](../entity_action_types.md)

Emits a 'game event' at the entity's position.

Type ID: `origins:emit_game_event`


!!! note

    See [Minecraft Fandom: Sculk Sensor (Vibration amplitudes)](https://minecraft.fandom.com/wiki/Sculk_Sensor?oldid=2099339#Vibration_amplitudes) for a list of vanilla game events you can use.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`event` | [Identifier](../data_types/identifier.md) | | The namespace and ID of a game event.


### Examples

```json
"entity_action": {
    "type": "origins:emit_game_event",
    "event": "minecraft:ring_bell"
}
```
This example will emit a `minecraft:ring_bell` game event, which has a redstone signal output of 6.
