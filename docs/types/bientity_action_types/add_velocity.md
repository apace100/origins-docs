---
title: Add Velocity (Bi-entity Action Type)
date: 2021-11-03
---

# Add Velocity

[Bi-entity Action Type](../bientity_action_types.md)

Adds or sets the velocity of the target entity, based on the direction from the actor entity to the target entity.

Type ID: `origins:add_velocity`

!!! note

    If the action behaves unexpectedly, try setting either the `client` (should always work) or `server` (might not work) boolean fields to `false`. [Here are some examples.](https://github.com/apace100/apoli/blob/3115c41ea4390ad9ced3ae5be86151131accc36f/testdata/apoli/powers/add_velocity.json)


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`x` | [Float](../data_types/float.md) | `0.0` | The amount of velocity to add on the x-axis.
`y` | [Float](../data_types/float.md) | `0.0` | The amount of velocity to add on the y-axis.
`z` | [Float](../data_types/float.md) | `0.0` | The amount of velocity to add on the z-axis.
`client` | [Boolean](../data_types/boolean.md) | `true` | If this is false, the action will not execute on the client.
`server` | [Boolean](../data_types/boolean.md) | `true` | If this is false, the action will not execute on the server.
`set` | [Boolean](../data_types/boolean.md) | `false` | If this is true, the action will act as a "set" velocity action, overriding the entity's current velocity instead of adding to it.


### Examples

```json
"bientity_action": {
    "type": "origins:add_velocity",
    "z": -2
}
```

This example will "pull" the target entity to the actor entity.
