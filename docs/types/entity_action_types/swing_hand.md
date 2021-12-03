---
title: Swing Hand (Entity Action Type)
date: 2021-11-30
---

# Swing Hand

[Entity Action Type](../entity_action_types.md)

Swings the specified hand.

Type ID: `origins:swing_hand`

!!! note

    This action is purely cosmetic, and will not interact with the world in any way. This means you can't use this to break, or place blocks, hit or use entities, or any other action that involves swinging your hand.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`hand` | [String](../data_types/string.md) | `MAIN_HAND` | Determines which hand is swung. Accepts either `"MAIN_HAND"`, `"OFF_HAND"`



### Examples

```json
"entity_action": {
    "type": "origins:swing_hand",
    "hand": "OFF_HAND"
}
```

This example will swing the entity's off hand.
