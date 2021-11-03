---
title: Add Velocity (Bi-entity Action)
date: 2021-10-06
---

# Add Velocity

[Bi-entity Action](../bientity_actions.md)

Adds or sets the velocity of the target entity, based on the direction from the actor entity to the target entity.

Type ID: `origins:add_velocity`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`x` | [Float](../data_types/float.md) | `0` | The amount of velocity to add on the x-axis.
`y` | [Float](../data_types/float.md) | `0` | The amount of velocity to add on the y-axis.
`z` | [Float](../data_types/float.md) | `0` | The amount of velocity to add on the z-axis.
`client` | [Boolean](../data_types/boolean.md) | true | If this is false, the action will not execute on the client.
`server` | [Boolean](../data_types/boolean.md) | true | If this is false, the action will not execute on the server.
`set` | [Boolean](../data_types/boolean.md) | false | If this is true, the action will act as a "set" velocity action, overriding the entity's current velocity instead of adding to it.

### Example
```json
"bientity_action": {
  "type": "origins:add_velocity",
  "z": -2
}
```
Pulls the target of the action towards the actor.
