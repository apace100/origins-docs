---
title: Status Effect
date: 2021-04-04
---
# Status Effect

[Entity Condition](../entity_conditions.md).

Checks whether the player has a specific status effect in a given amplifier and/or duration range.

Type ID: `origins:status_effect`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [String](../data_types/comparison.md) | | _ID of the status effect the player should have._
`min_amplifier` | [Integer](../data_types/integer.md) | `0` | _The minimum amplifier the status effect should have in order to pass the check._
`max_amplifier` | [Integer](../data_types/integer.md) | `2147483647` | _The maximum amplifier the status effect should have in order to pass the check._
`min_duration` | [Integer](../data_types/integer.md) | `0` | _The minimum duration in ticks the status effect should have left in order to pass the check._
`max_duration` | [Integer](../data_types/integer.md) | `2147483647` | _The maximum duration in ticks the status effect should have left in order to pass the check._
