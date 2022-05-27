---
title: Origin (Entity Condition Type)
date: 2021-04-04
---

# Origin

[Entity Condition Type](../entity_condition_types.md)

Checks whether the player has a certain origin (optionally from a certain layer).

Type ID: `origins:origin`


!!! caution

    Make sure to use the [Entity Type (Entity Condition Type)](entity_type.md) to check if the entity is a Player entity, otherwise, the game will crash since only Players can have origins.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`origin` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the origin the player needs to have to pass the check.
`layer` | [Identifier](../data_types/identifier.md) | _optional_ |  If specified, the condition will check if the origin is from the specified origin layer.


### Examples

```json
"condition": {
    "type": "origins:origin",
    "origin": "origins:human",
    "layer": "origins:origin"
}
```

This example will check if the player has the `origins:human` origin that is provided by the `origins:origin` origin layer.
