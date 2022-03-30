---
title: Origin (Entity Condition Type)
date: 2021-04-04
---

# Origin

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity has a certain origin (optionally in a certain layer). Mostly used for [Origin conditions in layers](../../guides/data/origin_conditions_in_layers.md).

Type ID: `origins:origin`

!!! note

    **This entity condition type will only work on players.**

!!! caution

    Using this Entity Condition on a non-player Entity will most likely crash the game. To prevent that make sure to check if the entity is a player by using the [Entity Type (Entity Condition Type)](entity_type.md) to prevent your game from crashing.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`origin` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the origin the player needs to have to pass the check.
`layer` | [Identifier](../data_types/identifier.md) | _optional_ |  If specified, only evaluate the condition to true if the origin is from the specified origin layer.


### Examples

```json
"condition": {
    "type": "origins:origin",
    "origin": "origins:human",
    "layer": "origins:origin"
}
```

This example will check if the player has the `origins:human` origin that is provided by the `origins:origin` origin layer.
