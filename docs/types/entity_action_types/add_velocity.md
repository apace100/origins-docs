---
title: Add Velocity (Entity Action Type)
date: 2021-11-03
---

# Add Velocity

[Entity Action Type](../entity_action_types.md)

Adds or sets velocity towards a specific direction.

Type ID: `origins:add_velocity`


### Fields

Field       |   Type                                |   Default                                                 |   Description
------------|---------------------------------------|-----------------------------------------------------------|--------------
`x`         |   [Float](../data_types/float.md)     |   <span style="color:chocolate"><b>DEPRECATED</b></span>  |   **Use the `velocity` field instead.**
`y`         |   [Float](../data_types/float.md)     |   <span style="color:chocolate"><b>DEPRECATED</b></span>  |   **Use the `velocity` field instead.**
`z`         |   [Float](../data_types/float.md)     |   <span style="color:chocolate"><b>DEPRECATED</b></span>  |   **Use the `velocity` field instead.**
`velocity`  |   [Vector](../data_types/vector.md)   |   `{"x": 0.0, "y": 0.0, "z": 0.0}`                        |   The amount of velocity to add.
`space`     |   [Space](../data_types/space.md)     |   `"position"`                                            |   Determines the direction of the velocity.
`client`    |   [Boolean](../data_types/boolean.md) |   <span style="color:darkred"><b>REMOVED</b></span>       |   **Use the [Side (Meta Action Type)](../meta_action_types/side.md) instead.**
`server`    |   [Boolean](../data_types/boolean.md) |   <span style="color:darkred"><b>REMOVED</b></span>       |   **Use the [Side (Meta Action Type)](../meta_action_types/side.md) instead.**
`set`       |   [Boolean](../data_types/boolean.md) |   `false`                                                 |   Determines whether the entity's velocity is overridden.


### Examples

```json
"entity_action": {
    "type": "origins:add_velocity",
    "velocity": {
        "y": 2
    }
}
```

This example will add velocity to the entity's positive Y axis, essentially launching the entity up in the air.
