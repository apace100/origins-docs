---
title: Modify Death Ticks (Entity Action Type)
date: 2022-07-03
---

#   Modify Death Ticks

[Entity Action Type](../entity_action_types.md)

Modifies how long the entity has been dead for.

Type ID: `origins:modify_death_ticks`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | | This modifier will be applied to the current death ticks value of the entity.


### Examples

```json
"entity_action": {
    "type": "origins:modify_death_ticks",
    "modifier": {
        "operation": "set_total",
        "value": 0
    }
}
```

This example will make the corpse of the entity remain in the world forever.
