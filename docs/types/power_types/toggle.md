---
title: Toggle (Power Type)
date: 2021-04-07
---

# Toggle

[Power Type](../power_types.md)

Provides a switch that can be toggled ON and OFF with the specified [Key](../data_types/key.md).

Type ID: `origins:toggle`


!!! note

    To check if the power with this power type is toggled ON (or OFF), you can use the [Power Active (Entity Condition Type)](../entity_condition_types/power_active.md).


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`active_by_default` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the state of this power type should be ON by default.
`key` | [Key](../data_types/key.md) | `{"key": "key.origins.primary_active"}` | Which active key this power should respond to.
`retain_state` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the state of this power type should retain if the condition (if there is any) is no longer fulfilled.


### Examples

```json
{
    "type": "origins:toggle",
    "active_by_default": false,
    "key": {
        "key": "key.use"
    }
}
```

This example will provide a switch that is not active by default, and can be toggled with the `key.use` keybind.
<br>

```json
{
    "type": "origins:toggle",
    "active_by_default": true,
    "retain_state": true,
    "key": {
        "key": "key.attack"
    },
    "condition": {
        "type": "origins:sneaking"
    }
}
```

This example will provide a switch that is active by default and can be toggled via sneaking and pressing the `key.attack` keybind. This example will also retain its state if the entity is no longer sneaking.
