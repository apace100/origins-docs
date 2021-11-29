---
title: Set On Fire (Entity Action Type)
date: 2021-04-05
---

# Set On Fire

[Entity Action Type](../entity_action_types.md)

Sets the entity on fire for the specified amount of time in seconds.

Type ID: `origins:set_on_fire`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`duration` | [Integer](../data_types/integer.md) |  | The amount of seconds the entity should burn.


### Examples

```json
"entity_action": {
    "type": "origins:set_on_fire",
    "duration": 5
}
```

This example will set the entity on fire for 5 seconds.
