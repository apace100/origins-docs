---
title: AND Action
date: 2021-04-06
---
# AND Action

[Meta Action](../meta_actions.md).

Usable as any action. Executes all provided actions in order.

Type ID: `origins:and`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`actions` | [Array](../data_types/array.md) | | An array of [Actions](../actions.md) of the same type. All of these will be executed one after the other.

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
