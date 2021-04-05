---
title: Resource
date: 2021-04-04
---
# Resource

[Entity Condition](../entity_conditions.md).

Checks the value of a [Resource (Power Type)](../power_types/resource.md) or a power with a cooldown (using the remaining ticks as the value).

Type ID: `origins:resource`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`resource` | [Identifier](../data_types/identifier.md) | | _ID of the power type that defines the resource. Must be a [Resource (Power Type)](../power_types/resource.md) which exists on the player._
`comparison` | [Comparison](../data_types/comparison.md) | | _How the resource should be compared to the specified value._
`compare_to` | [Integer](../data_types/integer.md) | | _Which value the resource should be compared to._
