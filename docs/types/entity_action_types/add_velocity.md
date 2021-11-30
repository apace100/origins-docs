---
title: Add Velocity (Entity Action Type)
date: 2021-11-03
---

# Add Velocity

[Entity Action Type](../entity_action_types.md)

Adds or sets velocity towards a specific direction.

Type ID: `origins:add_velocity`

!!! note

    If the action behaves unexpectedly, try setting either the `client` (should always work0 or `server` (might not work) boolean fields to `false`. [Here are some examples.](https://github.com/apace100/apoli/blob/3115c41ea4390ad9ced3ae5be86151131accc36f/testdata/apoli/powers/add_velocity.json)


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`x` | [Float](../data_types/float.md) | `0` | The amount of velocity to add on the x-axis.
`y` | [Float](../data_types/float.md) | `0` | The amount of velocity to add on the y-axis.
`z` | [Float](../data_types/float.md) | `0` | The amount of velocity to add on the z-axis.
`space` | [String](../data_types/string.md) | `"world"` | The [Space](../../misc/extras/space.md) to perform the velocity addition in.
`client` | [Boolean](../data_types/boolean.md) | `true` | If this is false, the action will not execute on the client.
`server` | [Boolean](../data_types/boolean.md) | `true` | If this is false, the action will not execute on the server.
`set` | [Boolean](../data_types/boolean.md) | `false` | If this is true, the action will act as a "set" velocity action, overriding the entity's current velocity instead of adding to it.



### Examples

```json
"entity_action": {
    "type": "origins:add_velocity",
    "y": 2
}
```

This example will add velocity to the entity's positive Y axis, essentially launching the entity up in the air.
