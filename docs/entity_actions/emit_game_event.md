---
title: Emit Game Event (Entity Action)
date: 2021-10-03
---
# Emit Game Event

[Entity Action](../entity_actions.md)

Emits a 'game event' at the entity. [See here for valid game events ID that you can use.](https://minecraft.fandom.com/wiki/Sculk_Sensor#Vibration_amplitudes)

Type ID: `origins:emit_game_event`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`event` | [Identifier](../data_types/identifier.md) | | The ID of a game event.

### Example
```json
"entity_action": {
    "type": "origins:emit_game_event",
    "event": "minecraft:ring_bell"
}
```
This example emits a `minecraft:ring_bell` game event, which has a redstone signal output of 6.