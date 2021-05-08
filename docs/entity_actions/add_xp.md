---
title: Add XP (Action)
date: 2021-04-05
---
# Add XP

[Entity Action](../entity_actions.md).

Adds experience points and levels to the player, or subtracts levels.

Type ID: `origins:add_xp`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`points` | [Integer](../data_types/integer.md) | _optional_ | If set, this is the amount experience points that will be given to the player. Can not be negative.
`levels` | [Integer](../data_types/integer.md) | _optional_ | If set, this is the amount experience levels that will be given to the player. Can be negative and thus used to subtract levels.

### Example
```json
"entity_action": {
    "type": "origins:add_xp",
    "levels": 2
}
```
This action adds 2 levels to the player.