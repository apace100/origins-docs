---
title: Modify Insomnia Ticks (Power Type)
date: 2022-06-07
---

# Modify Insomnia Ticks

[Power Type](../power_types.md)

Modifies the value used for calculating when a Phantom will spawn for a player.

Type ID: `origins:modify_insomnia_ticks`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the value.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the value.


### Examples

```json
{
    "type": "origins:modify_insomnia_ticks",
    "modifier": {
        "operation": "set_total",
        "value": 0
    }
}
```

This example will set the value used for calculating when a Phantom will spawn for a player to 0, essentially disabling Phantoms from spawning for the player that has the power.
