---
title: Ability (Entity Condition Type)
date: 2021-12-07
---

# Ability

[Entity Condition Type](../entity_condition_types.md)

Checks if the entity has the specified ability enabled.

Type ID: `apoli:ability`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`ability` | [String](../data_types/string.md) | | The namespace and ID of the ability to check for.


### Examples

```json
"condition": {
    "type": "apoli:ability",
    "ability": "minecraft:mayfly"
}
```

This example will check if the player can fly in a Creative Mode-like fashion.
