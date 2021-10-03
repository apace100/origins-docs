---
title: Prevent Game Event (Power Type)
date: 2021-10-03
---
# Prevent Game Event

[Power Type](../power_types.md)

Prevents specified game event(s) from being emitted by the entity.

Type ID: `origins:prevent_game_event`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`event` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the game event with this ID will be prevented from being emitted by the entity.
`events` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, the game events with these IDs will be prevented from being emitted by the entity.
`tag` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the game events inside this game event tag will be prevented from being emitted by the entity.
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the entity if the specified game events are prevented.

### Example
```json
{
    "type": "origins:prevent_game_event",
    "event": "minecraft:hit_ground",
    "entity_action": {
        "type": "origins:execute_command",
        "command": "say donk"
    }
}
```
This example prevents the entity that has the power to emit a `minecraft:hit_ground` game event, which is usually emitted by landing on the ground upon falling, and runs a `/say` command.