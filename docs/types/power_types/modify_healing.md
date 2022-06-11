---
title: Modify Healing (Power Type)
date: 2022-06-07
---

# Modify Healing

[Power Type](../power_types.md)

Modifies the amount of health you get from all sources of healing _(e.g natural regen, instant health effect, regeneration effect)_

Type ID: `origins:modify_healing`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to your healing bonus.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to your healing bonus.

### Examples

```json
{
    "type": "origins:modify_healing",
    "modifier": {
        "operation": "multiply_total",
        "value": 1
    }
}
```

This example will double the effectiveness of all healing used on you.
```json
{
    "type": "origins:modify_healing",
    "modifier": {
        "operation": "multiply_total",
        "value": -0.5
    }
}
```

This example will half the effectiveness of all healing used on you.
