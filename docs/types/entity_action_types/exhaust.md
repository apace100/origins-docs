---
title: Exhaust (Entity Action Type)
date: 2021-04-05
---

# Exhaust

[Entity Action Type](../entity_action_types.md)

Applies exhaustion to the entity, reducing saturation and hunger.

Type ID: `origins:exhaust`

!!! note

    **This entity action type will only work on players.**


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`amount` | [Float](../data_types/float.md) |  | The amount of exhaustion to apply to the player.


### Examples

```json
"entity_action": {
    "type": "origins:exhaust",
    "amount": 0.4
}
```

This example will apply 0.4 exhaustion to the player, which is similar in effect to jumping 8 times (without sprinting).
