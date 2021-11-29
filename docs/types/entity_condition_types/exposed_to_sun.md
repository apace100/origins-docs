---
title: Exposed to Sun (Entity Condition Type)
date: 2021-04-04
---

# Exposed to Sun

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity is currently exposed to the sun, which is essentially a mix of [Brightness (Entity Condition Type)](brightness.md) that checks if the brightness level at the entity's eyes is greather than 0.5 and [Exposed to Sky (Entity Condition Type)](exposed_to_sky.md).

Type ID: `origins:exposed_to_sun`


### Fields

_None._


### Examples

```json
"condition": {
    "type": "origins:exposed_to_sun"
}
```
