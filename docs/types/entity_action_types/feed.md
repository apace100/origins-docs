---
title: Feed (Entity Action Type)
date: 2021-04-05
---

# Feed

[Entity Action Type](../entity_action_types.md)

Feeds the entity, filling up their hunger bar as if they had eaten a food item with the provided values.

Type ID: `origins:feed`

!!! note

    The actual food saturation level is determined by the `food * saturation * 2` formula.

!!! note

    This entity action type will **only** work on players.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`food` | [Integer](../data_types/integer.md) |  | The food amount to restore.
`saturation` | [Float](../data_types/float.md) |  | The saturation amount to restore.

### Example
```json
"entity_action": {
    "type": "origins:feed",
    "food": 4,
    "saturation": 2
}
```
This action *feeds* the player 2 hunger shanks (4 hunger points), and 16 saturation points.