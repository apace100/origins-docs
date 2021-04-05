---
title: Heal (Action)
date: 2021-04-05
---
# Heal

[Entity Action](../entity_actions.md).

Heals an entity.

Type ID: `origins:heal`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`amount` | [Float](../data_types/float.md) |  | The amount of health to restore.


### Example
```json
"entity_action": {
  "type": "origins:heal",
  "amount": 6
}
```
This action heals the target entity for 3 hearts.
