---
title: Power Active (Entity Condition Type)
date: 2021-04-04
---

# Power Active

[Entity Condition Type](../entity_condition_types.md)

Checks whether the specified power is "active", meaning that the entity has the power and the power has all its conditions fulfilled.

Type ID: `apoli:power_active`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power which will be checked for being active.


### Examples

```json
"condition": {
    "type": "apoli:power_active",
    "power": "test:toggle"
}
```

This example will check if the `test:toggle` power is toggled on.
