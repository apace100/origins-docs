---
title: And (Meta Action Type)
date: 2021-04-06
---

# And

[Meta Action Type](../meta_action_types.md)

Executes all provided actions in order.

Type ID: `origins:and`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`actions` | [Array](../data_types/array.md) of [Actions](../action_types.md) | | These actions will be executed one after the other (but in the same tick).

### Example

```json
"entity_action": {
    "type": "origins:and",
    "actions": [
        {
            "type": "origins:exhaust",
            "amount": 0.5
        },
        {    
            "type": "origins:apply_effect",
            "effect": {
            "effect": "minecraft:regeneration",
            "amplifier": 1,
            "duration": 100
            }
        }
    ]
}
```

This action will exhaust the player (reduce their saturation/food level) and then immediately apply a 5 second Regeneration II effect.
