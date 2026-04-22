---
title: Add Velocity (Bi-entity Action Type)
date: 2021-11-03
---

# Add Velocity

[Bi-entity Action Type](../bientity_action_types.md)

Adds or sets the velocity of the target entity, based on the direction from the actor entity to the target entity.

Type ID: `origins:add_velocity`


### Fields

Field       |   Type                                |   Default                                                 |   Description
------------|---------------------------------------|-----------------------------------------------------------|--------------
`x`         |   [Float](../data_types/float.md)     |   <span style="color:chocolate"><b>DEPRECATED</b></span>  |   **Use the `velocity` field instead.**
`y`         |   [Float](../data_types/float.md)     |   <span style="color:chocolate"><b>DEPRECATED</b></span>  |   **Use the `velocity` field instead.**
`z`         |   [Float](../data_types/float.md)     |   <span style="color:chocolate"><b>DEPRECATED</b></span>  |   **Use the `velocity` field instead.**
`velocity`  |   [Vector](../data_types/vector.md)   |   `{"x": 0.0, "y": 0.0, "z": 0.0}`                        |   The amount of velocity to add.
`reference` |   [String](../data_types/string.md)   |   `"position"`                                            |   Determines whether to use the actor entity's `"position"` or `"rotation"` when calculating the velocity that will be applied to the target entity.
`client`    |   [Boolean](../data_types/boolean.md) |   <span style="color:darkred"><b>REMOVED</b></span>       |   **Use the [Side (Meta Action Type)](../meta_action_types/side.md) instead.**
`server`    |   [Boolean](../data_types/boolean.md) |   <span style="color:darkred"><b>REMOVED</b></span>       |   **Use the [Side (Meta Action Type)](../meta_action_types/side.md) instead.**
`set`       |   [Boolean](../data_types/boolean.md) |   `false`                                                 |   Determines whether the target entity's velocity is overridden


### Examples

```json
"bientity_action": {
    "type": "origins:add_velocity",
    "velocity": {
        "z": -2
    }
}
```

This example will "pull" the target entity to the actor entity.
