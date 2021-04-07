---
title: Constant (Condition)
date: 2021-04-07
---
# Constant

[Meta Condition](../meta_conditions.md).

This condition is either always fulfilled or always not fulfilled. Mainly added as a backup in case a condition isn't optional in some place.

Type ID: `origins:constant`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`value` | [Boolean](../data_types/boolean.md) | | If true, the condition is always fulfilled. If false, the condition is never fulfilled.

### Example

```json
"condition": {
  "type": "origins:constant",
  "value": true
}
```
This condition is always true.
