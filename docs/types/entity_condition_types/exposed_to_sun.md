---
title: Exposed to Sun (Entity Condition Type)
date: 2021-04-04
---

# Exposed to Sun

[Entity Condition Type](../entity_condition_types.md)

Checks whether the player is currently exposed to the sun. Essentially a [Brightness](brightness.md) check for `brightness > 0.5` combined with and an [Exposed to Sky](exposed_to_sky.md) check.

Type ID: `origins:exposed_to_sun`

### Fields:

_None._

### Example:
```json
"condition": {
    "type": "origins:exposed_to_sun"
}
```
