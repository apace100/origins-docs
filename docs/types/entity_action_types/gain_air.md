---
title: Gain Air (Entity Action Type)
date: 2021-04-05
---

# Gain Air

[Entity Action Type](../entity_action_types.md)

Restores breath (bubbles!) to a living entity.

Type ID: `apoli:gain_air`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`value` | [Integer](../data_types/integer.md) |  | The amount of breath to restore.


### Examples

```json
"entity_action": {
    "type": "apoli:gain_air",
    "value": 20
}
```

This example will restore about 1 second of breath to the entity.
