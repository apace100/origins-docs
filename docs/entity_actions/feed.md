---
title: Feed (Action)
date: 2021-04-05
---
# Feed

[Entity Action](../entity_actions.md).

Feeds the player, filling up their hunger bar as if they had eaten a food item with the provided values.

Type ID: `origins:feed`

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
This action *feeds* the player 2 hunger shanks (4 hunger points), and 2 saturation points.