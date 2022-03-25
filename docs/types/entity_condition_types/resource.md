---
title: Resource (Entity Condition Type)
date: 2021-04-04
---

# Resource

[Entity Condition Type](../entity_condition_types.md)

Checks the value of a power that uses the [Resource (Power Type)](../power_types/resource.md) or a power type that has a built-in cooldown (using remaining ticks as the value).

Type ID: `apoli:resource`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`resource` | [Identifier](../data_types/identifier.md) | | The namespace and ID of a power that will be evaluated.
`comparison` | [Comparison](../data_types/comparison.md) | | How the value of the power that will be evaluated should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value to compare the value of the power that will be evaluated to.


### Examples

```json
"condition": {
    "type": "apoli:resource",
    "resource": "test:example_resource",
    "comparison": "==",
    "compare_to": 1
}
```

This example will check if the player has a value of 1 in the `test:example_resource` resource power. (`data\test\powers\example_resource.json`)
<br>

```json
"condition": {
    "type": "apoli:resource",
    "resource": "test:a_multiple_power_with_resource_subpower",
    "comparison": ">",
    "compare_to": 50
}
```

This example will check if the player has a value of more than 50 in the `with_resource_subpower` sub-power of `test:a_multiple_power` power. (`data\test\powers\a_multiple_power.json`)
