---
title: Choice (Action)
date: 2021-04-07
---
# Choice

[Meta Action](../meta_actions.md).

Executes one of the provided actions, choosing randomly based on the assigned weights. The actions with higher weight values are more likely to be chosen.

Type ID: `origins:choice`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`actions` | [Array](../data_types/array.md) | | Array of [Objects](../data_types/object.md), each with an `element` [Action](../actions.md) and a `weight` [Integer](../data_types/integer.md).

### Example

```json
"entity_action": {
  "type": "origins:choice",
  "actions": [
    {
      "element": {
        "type": "origins:exhaust",
        "amount": 0.5
      },
      "weight": 10
    },
    {
      "element": {    
        "type": "origins:apply_effect",
        "effect": {
          "effect": "minecraft:regeneration",
          "amplifier": 1,
          "duration": 100
        }
      },
      "weight": 10
    },
    {
      "element": {
        "type": "origins:set_on_fire",
        "duration": 8
      },
      "weight": 20
    }
  ]
}
```

With a chance of 25% (weight / sum of all weights), this action will exhaust the player. With a chance of 25%, it will apply a regeneration effect. With a chance of 50%, it will set the player on fire for 8 seconds.
