---
title: Constant (Meta Condition Type)
date: 2021-04-07
---

# Constant

[Meta Condition Type](../meta_condition_types.md)

Provides a constant state where it's either true or false. Mainly added as a backup case in case a condition is required in some power/action/condition types.

Type ID: `origins:constant`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`value` | [Boolean](../data_types/boolean.md) | | If true, the condition is always fulfilled. If false, the condition is never fulfilled.


### Examples

```json
"condition": {
    "type": "origins:constant",
    "value": true
}
```

This example is always true.
