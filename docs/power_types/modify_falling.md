---
title: Modify Falling (Power Type)
date: 2021-07-06
---

# Modify Falling

[Power Type](../power_types.md)

Modifies player's falling velocity, and whether if the player should take fall damage or not.
By default, the player falls at a speed of 0.08, or 0.01 if a slow falling potion is active.

Type ID: `origins:modify_falling`

### Fields:

Field              | Type                                | Default | Description
-------------------|-------------------------------------|---------|------------
`velocity`         | [Float](../data_types/float.md)     |         | How slow/fast the falling velocity should be.
`take_fall_damage` | [Boolean](../data_types/boolean.md) | true    | Whether the player should take fall damage or not.

### Example:

```json
{
    "type": "origins:modify_falling",
    "velocity": 1.0,
    "take_fall_damage": false,
    "condition": {
        "type": "origins:sneaking"
    }
}
```
Makes the player fall faster and not take fall damage if they're sneaking.
