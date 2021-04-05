---
title: Add Velocity (Action)
date: 2021-04-05
---
# Add Velocity

[Entity Action](../entity_actions.md).

Adds velocity towards a specific direction.

Type ID: `origins:add_velocity`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`x` | [Float](../data_types/float.md) | `0` | The amount of velocity to add on the x-axis.
`y` | [Float](../data_types/float.md) | `0` | The amount of velocity to add on the y-axis.
`z` | [Float](../data_types/float.md) | `0` | The amount of velocity to add on the z-axis.
`space` | [String](..data_types/string.md) | _"world"_ | The [Space](../misc/space.md) to perform the velocity addition in.

### Example
```json
"entity_action": {
  "type": "origins:add_velocity",
  "y": 2
}
```
Launches the entity upwards into the air.
