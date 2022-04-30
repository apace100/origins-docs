---
title: Elytra Flight Possible
date: 2021-12-01
---

# Elytra Flight Possible

[Entity Condition Type](../entity_condition_types.md)

Checks if the entity can fly with either an Elytra item or a power that uses the [Elytra Flight (Power Type)](../power_types/elytra_flight.md).

Type ID: `origins:elytra_flight_possible`


!!! note

    If both `check_state` and `check_abilities` boolean fields are set to `true`, the entity condition type will check if the player can activate elytra flight at the very moment.

!!!  warning

    If both `check_state` and `check_abilities` boolean fields are set to `false`, the entity condition type will evaluate to true.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`check_state` | [Boolean](../data_types/boolean.md) | `false` | If set to `true`, the entity condition type will check if pressing the `key.jump` keybind would activate elytra flight if the player had the ability to.
`check_abilities` | [Boolean](../data_types/boolean.md) | `true` | If set to `true`, the entity condition type will check whether the player has the ability to activate elytra flight. (e.g: wearing an elytra or have a power that uses the [Elytra Flight (Power Type)](../power_types/elytra_flight.md))


### Examples

```json
"condition": {
    "type": "origins:elytra_flight_possible",
    "check_state": true,
    "check_abilities": true
}
```

This example will check if the player can activate elytra flight.
