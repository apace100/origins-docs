---
title: Dimension (Entity Condition Type)
date: 2021-04-04
---

# Dimension

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity is in a specified dimension.

Type ID: `apoli:dimension`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`dimension` | [Identifier](../data_types/identifier.md) | |  The namespace and ID of the dimension the player needs to be in for this condition to evaluate to true. Vanilla dimensions are `minecraft:overworld`, `minecraft:the_nether` and `minecraft:the_end`, but namespace and IDs of custom/modded dimensions should also work.


### Examples

```json
"condition": {
    "type": "apoli:dimension",
    "dimension": "minecraft:overworld",
    "inverted": true
}
```

This example will check if the player is **not** in the Overworld dimension.
