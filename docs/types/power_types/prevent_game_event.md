---
title: Prevent Game Event (Power Type)
date: 2021-10-03
---

# Prevent Game Event

[Power Type](../power_types.md)

Prevents specified game event(s) from being emitted by the entity that has the power.

Type ID: `origins:prevent_game_event`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`event` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the game event with this namespace and ID will be prevent from being emitted by the entity.
`events` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, the game events with these namespace and IDs will be prevent from being emitted by the entity.
`tag` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the game events inside game event tag will be prevented from being emitted by the entity.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity upon preventing game events.


### Examples

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

This example will prevent the entity that has the power to emit a `minecraft:hit_ground` game event, which is usually emitted by landing on the ground upon falling.
