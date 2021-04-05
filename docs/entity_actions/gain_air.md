---
title: Gain Air (Action)
date: 2021-04-05
---
# Gain Air

[Entity Action](../entity_actions.md).

Restores breath (bubbles!) to a living entity.

Type ID: `origins:gain_air`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`value` | [Integer](../data_types/integer.md) |  | The amount of breath to restore.

### Example
```json
"entity_action": {
  "type": "origins:gain_air",
  "value": 20
}
```
This action restores about 1 second of breath.
