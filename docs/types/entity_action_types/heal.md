---
title: Heal (Entity Action Type)
date: 2021-04-05
---

# Heal

[Entity Action Type](../entity_action_types.md)

Restores a specified amount of health to the entity.

Type ID: `origins:heal`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`amount` | [Float](../data_types/float.md) |  | The amount of health to restore.


### Examples

```json
"entity_action": {
    "type": "origins:heal",
    "amount": 6
}
```

This example will restore about 3 hearts to the entity.
