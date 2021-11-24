---
title: And (Meta Condition Type)
date: 2021-04-07
---

# And

[Meta Condition Type](../meta_condition_types.md)

This condition checks whether all of the provided conditions are fulfilled.

Type ID: `origins:and`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`conditions` | [Array](../types/data_types/array.md) of [Conditions](../conditions.md) | | All of these conditions have to be fulfilled in order for this condition to be fulfilled.

### Example

```json
"condition": {
  "type": "origins:and",
  "conditions": [
    {
      "type": "origins:daytime"
    },
    {      
      "type": "origins:invisible"
    }
  ]
}
```
This condition added to a power will make sure the power is only active when it is both day and the player is invisible.
