---
title: Bonemeal (Block Action Types)
date: 2021-12-02
---

# Bonemeal

[Block Action Type](../block_action_types.md)

Applies bone meal to the target block as if a dispenser or a player used a Bone Meal item to it.

Type ID: `origins:bonemeal`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`effects` | [Boolean](../data_types/boolean.md) | `true` | Determines if the particle and other visual effects of the bonemeal-ing action should appear.


### Examples

```json
"block_action": {
    "type": "origins:bonemeal",
    "effects": false
}
```

This example will apply bonemeal to the target block of the block action without the visual effects.
