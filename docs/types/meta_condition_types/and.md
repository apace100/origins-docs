---
title: And (Meta Condition Type)
date: 2021-04-07
---

# And

[Meta Condition Type](../meta_condition_types.md)

Checks whether all of the provided conditions are fulfilled.

Type ID: `origins:and`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`conditions` | [Array](../data_types/array.md) of [Condition Types](../condition_types.md) | | All of these condition types have to be fulfilled in order for this condition to be fulfilled.


### Examples

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

This example will check if it is both daytime, and the entity is invisible.
