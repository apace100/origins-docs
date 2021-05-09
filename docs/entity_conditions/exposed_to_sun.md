---
title: Exposed to Sun
date: 2021-04-04
---
# Exposed to Sun

[Entity Condition](../entity_conditions.md).

Checks whether the player is currently exposed to the sun. Essentially a [Brightness](../entity_conditions/brightness) check for `brightness > 0.5` combined with and an [Exposed to Sky](../entity_conditions/exposed_to_sky) check.

Type ID: `origins:exposed_to_sun`

### Fields:

_None._

### Example:
```json
"condition": {
    "type": "origins:exposed_to_sun"
}
```