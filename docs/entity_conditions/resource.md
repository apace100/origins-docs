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

### Examples:
```json
"condition": {
    "type": "origins:resource",
    "resource": "example:a_simple_resource",
    "comparison": "==",
    "compare_to": 1
}
```
This example checks if the player has a value of 1 in the `example:a_simple_resource` resource power. (`data\example\powers\a_simple_resource.json`)


```json
"condition": {
    "type": "origins:resource",
    "resource": "example:a_multiple_power_with_resource_subpower",
    "comparison": ">",
    "compare_to": 50
}
```
This example checks if the player has a value of 50 or more in the `with_resource_subpower` sub-power of `example:a_multiple_power` power. (`data\example\powers\a_multiple_power.json`)