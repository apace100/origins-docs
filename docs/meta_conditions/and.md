---
title: And (Condition)
date: 2021-04-07
---
# And

[Meta Condition](../meta_conditions.md).

This condition checks whether all of the provided conditions are fulfilled.

Type ID: `origins:and`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`conditions` | [Array](../data_types/array.md) of [Conditions](../conditions.md) | | All of these conditions have to be fulfilled in order for this condition to be fulfilled.

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
