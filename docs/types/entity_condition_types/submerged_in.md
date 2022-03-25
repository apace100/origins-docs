---
title: Submerged In (Entity Condition Type)
date: 2021-04-04
---

# Submerged In

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity's eyes are in a fluid that is included in the specified fluid tag.

Type ID: `apoli:submerged_in`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`fluid` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the fluid tag that should be checked. Most important examples: `minecraft:water` and `minecraft:lava`.


### Examples

```json
"condition": {
    "type": "apoli:submerged_in",
    "fluid": "minecraft:water"
}
```

This example will check if the player is submerged in water.
