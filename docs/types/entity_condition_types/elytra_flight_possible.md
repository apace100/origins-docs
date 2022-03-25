---
title: Elytra Flight Possible
date: 2021-12-01
---

# Elytra Flight Possible

[Entity Condition Type](../entity_condition_types.md)

Checks if the entity can fly with either an Elytra item or a power that uses the [Elytra Flight (Power Type)](../power_types/elytra_flight.md).

Type ID: `apoli:elytra_flight_possible`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`check_state` | [Boolean](../data_types/boolean.md) | `false` | Determines if the condition should check if the entity is currently flying with an elytra.
`check_abilities` | [Boolean](../data_types/boolean.md) | `true` | Determines if the condition should check if the entity can fly with an elytra.


### Examples

```json
"condition": {
    "type": "apoli:elytra_flight_possible",
    "check_state": true,
    "check_abilities": true
}
```

This example will check if the entity can fly with an elytra, and is currently flying with an elytra.
