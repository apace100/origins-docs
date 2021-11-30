---
title: Modify XP Gain (Power Type)
date: 2021-04-06
---

# Modify XP Gain

[Power Type](../power_types.md)

Modifies how much XP the player gains when they pick up an experience orb.

Type ID: `origins:modify_xp_gain`

!!! note

    Be careful not to make this go too high, as then the player would be able to gain more experience from dying.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the experience gained.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the experience gained.



### Examples

```json
{
    "type": "origins:modify_xp_gain",
    "modifier": {
        "operation": "multiply_base",
        "value": 2.0
    }
}
```

This example will triple the gained experience from experience orbs.
