---
title: Status Effect (Condition)
date: 2021-04-04
---
# Status Effect

[Entity Condition](../entity_conditions.md).

Checks whether the player has a specific status effect in a given amplifier and/or duration range.

Type ID: `origins:status_effect`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Identifier](../data_types/identifier.md) | | _ID of the status effect the player should have._
`min_amplifier` | [Integer](../data_types/integer.md) | `0` | The minimum amplifier the status effect should have in order to pass the check.
`max_amplifier` | [Integer](../data_types/integer.md) | `2147483647` | The maximum amplifier the status effect should have in order to pass the check.
`min_duration` | [Integer](../data_types/integer.md) | `0` | The minimum duration in ticks the status effect should have left in order to pass the check.
`max_duration` | [Integer](../data_types/integer.md) | `2147483647` | The maximum duration in ticks the status effect should have left in order to pass the check.

### Example:
```json
"condition": {
    "type": "origins:status_effect",
    "effect": "minecraft:speed",
    "min_amplifier": 1
}
```
This example checks if the player has the Speed II status effect.