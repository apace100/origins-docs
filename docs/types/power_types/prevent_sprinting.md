---
title: Prevent Sprinting (Power Type)
date: 2022-06-07
---

# Prevent Sprinting

[Power Type](../power_types.md)

Prevents the player with this power from sprinting if a condition is met.

Type ID: `origins:prevent_sprinting`

### Fields
_None._


### Examples

```json
{
  "type": "origins:prevent_sprinting",
  "condition": {
    "type": "origins:food_level",
    "compare_to": 12,
    "comparison": "<="
  }
}
```

This example will prevent the player from sprinting if their food level is at, or below 6 hunger shanks
