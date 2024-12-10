---
title: Toggle (Power Type)
date: 2021-04-07
---

# Toggle

[Power Type](../power_types.md)

Provides a state that can be toggled with the specified [Key](../data_types/key.md).

Type ID: `origins:toggle`


!!! note

    This power type provides a state that can be toggled with the [Toggle (Entity Action Type)](../entity_action_types/toggle.md) and check the state of with the [Power Active (Entity Condition Type)](../entity_condition_types/power_active.md).


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`active_by_default` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the state of this power type should be ON by default.
`key` | [Key](../data_types/key.md) | `{"key": "key.origins.primary_active"}` | Which active key this power should respond to.
`retain_state` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the power remains active even if the specified condition (if any) is no longer met. If set to `true`, the power will stay in its current state regardless of the condition. If set to `false`, the power will deactivate when the condition is not fulfilled.


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
