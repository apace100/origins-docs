---
title: Set On Fire (Action)
date: 2021-04-05
---
# Set On Fire

[Entity Action](../entity_actions.md).

Sets the entity to burn for a specified duration.

Type ID: `origins:set_on_fire`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`duration` | [Integer](../data_types/integer.md) |  | The amount of seconds the entity should burn.

### Example
```json
"entity_action": {
  "type": "origins:set_on_fire",
  "duration": 5
}
```
Sets the entity on fire for 5 seconds.
