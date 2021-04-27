---
title: Toggle (Power Type)
date: 2021-04-07
---
# Toggle

[Power Type](../power_types.md).

Defines a power which can be toggled on and off with the active power key. Can be used by coders with a `PowerTypeReference` to provide functionality, or by other powers with a [Power Active](../entity_conditions/power_active.md) condition.

Type ID: `origins:toggle`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`active_by_default` | [Boolean](../data_types/boolean.md) | `true` | Whether this power starts in the on or off state.
`key` | [Key](../data_types/key.md) | `primary` | Which active key this power should respond to.


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