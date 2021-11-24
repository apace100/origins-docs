---
title: Gamemode (Entity Condition Type)
date: 2021-04-06
---

# Gamemode

[Entity Condition Type](../entity_condition_types.md)

Checks the gamemode of a player. Will return false if the entity is not a player.

Type ID: `origins:gamemode`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`gamemode` | [String](../data_types/string.md) | | Name of the gamemode the player should have in order for this condition to evaluate to true.

### Example:

```json
"condition": {
  "type": "origins:gamemode",
  "gamemode": "creative"
}
```
This condition will only pass on players which are in creative mode.
