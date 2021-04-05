---
title: Resource (Condition)
date: 2021-04-04
---
# Resource

[Entity Condition](../entity_conditions.md).

Checks the value of a [Resource (Power Type)](../power_types/resource.md) or a power with a cooldown (using the remaining ticks as the value).

Type ID: `origins:resource`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`resource` | [Identifier](../data_types/identifier.md) | | ID of the power type that defines the resource. Must be a [Resource (Power Type)](../power_types/resource.md) which exists on the player.
`comparison` | [Comparison](../data_types/comparison.md) | | How the resource should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value the resource should be compared to.
