---
title: Power Type (Entity Condition Type)
date: 2021-12-01
---

# Power Type

[Entity Condition Type](../entity_condition_types.md)

Checks if the entity has a power that uses the specified power type.

Type ID: `origins:power_type`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power_type` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power type of a power the entity has.


### Examples

```json
"condition": {
    "type": "origins:power_type",
    "power_type": "origins:active_self"
}
```

This example will check if the entity has a power that uses the [Active Self (Power Type)](../power_types/active_self.md).
