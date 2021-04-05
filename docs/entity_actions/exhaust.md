---
title: Exhaust (Action)
date: 2021-04-05
---
# Exhaust

[Entity Action](../entity_actions.md).

Applies exhaustion to the player, reducing saturation and hunger. Only works on players.

Type ID: `origins:exhaust`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`amount` | [Float](../data_types/float.md) |  | The amount of exhaustion to apply to the player.

### Example
```json
"entity_action": {
  "type": "origins:exhaust",
  "amount": 0.4
}
```
This action applies 0.4 exhaustion, which is similar in effect to jumping 8 times (without sprinting).
