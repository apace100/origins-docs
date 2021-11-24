---
title: Toggle (Power Type)
date: 2021-04-07
---

# Toggle

[Power Type](../power_types.md)

Provides a switch that can be toggled ON and OFF with the specified [Key](../data_types/key.md).

Type ID: `origins:toggle`

!!! note

    To check if the power with this power type is toggled ON (or OFF), you can use the [Power Active](../entity_conditions/power_active.md) entity condition type.

!!! note

    This power type can be used by <u>**addon**</u> developers by creating a new `PowerTypeReference` to provide functionality.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`active_by_default` | [Boolean](../types/data_types/boolean.md) | `true` | Whether this power starts in the on or off state.
`key` | [Key](../data_types/key.md) | `{"key": "key.origins.primary_active"}` | Which active key this power should respond to.


### Example
```json
{
    "type": "origins:toggle",
    "active_by_default": false,
    "key": {
        "key": "key.use"
    }
}
```
This power is not active by default, and can be toggled by using the `key.use` keybind. Can be checked if the power is toggled on with the [`origins:power_active`](../entity_conditions/power_active.md) entity condition.