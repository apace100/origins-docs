---
title: Status Effect (Entity Condition Type)
date: 2021-04-04
---

# Status Effect

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity has a specified status effect with a specified amplifier, and/or duration range.

Type ID: `origins:status_effect`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the status effect to check for.
`min_amplifier` | [Integer](../data_types/integer.md) | `0` | The minimum amplifier the status effect should have in order to pass the check.
`max_amplifier` | [Integer](../data_types/integer.md) | `2147483647` | The maximum amplifier the status effect should have in order to pass the check.
`min_duration` | [Integer](../data_types/integer.md) | `0` | The minimum duration in ticks the status effect should have left in order to pass the check.
`max_duration` | [Integer](../data_types/integer.md) | `2147483647` | The maximum duration in ticks the status effect should have left in order to pass the check.


### Examples

```json
"condition": {
    "type": "origins:status_effect",
    "effect": "minecraft:speed",
    "min_amplifier": 1
}
```

This example will check if the entity has the Speed II status effect.
