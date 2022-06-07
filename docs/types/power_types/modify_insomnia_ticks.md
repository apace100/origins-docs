---
title: Modify Insomnia Ticks (Power Type)
date: 2022-06-07
---

# Modify Insomnia Ticks

[Power Type](../power_types.md)

Modifies the amount of time it takes for phantoms to spawn right before spawning them, as long as a condition is met. 

Type ID: `origins:modify_insomnia_ticks`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the phantom timer.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the phantom timer.

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

This example will reset the time needed for phantoms to spawn every time they try, effectively disabling them.
