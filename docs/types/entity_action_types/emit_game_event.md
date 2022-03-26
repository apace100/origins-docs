---
title: Emit Game Event (Entity Action Type)
date: 2021-10-03
---

# Emit Game Event

[Entity Action Type](../entity_action_types.md)

Emits a 'game event' at the entity's position.

Type ID: `origins:emit_game_event`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`event` | [Identifier](../data_types/identifier.md) | | The namespace and ID of a game event. See [Minecraft Fandom Wiki: Sculk Sensor (Vibration amplitudes)](https://minecraft.fandom.com/wiki/Sculk_Sensor#Vibration_amplitudes) for a list of game events you can use.


### Examples

```json
"entity_action": {
    "type": "origins:emit_game_event",
    "event": "minecraft:ring_bell"
}
```
This example will emit a `minecraft:ring_bell` game event, which has a redstone signal output of 6.
