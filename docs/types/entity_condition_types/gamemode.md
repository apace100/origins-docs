---
title: Gamemode (Entity Condition Type)
date: 2021-04-06
---

# Gamemode

[Entity Condition Type](../entity_condition_types.md)

Checks the gamemode of the entity.

Type ID: `origins:gamemode`

!!! note

    **This entity condition type will only work on players.**


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`gamemode` | [String](../data_types/string.md) | | Name of the gamemode the player should have in order for this condition to evaluate to true.


### Examples

```json
"condition": {
  "type": "origins:gamemode",
  "gamemode": "creative"
}
```

This example will check if the player is in Creative Mode.
