---
title: Set Fall Distance (Action)
date: 2021-04-06
---
# Set Fall Distance

[Entity Action](../entity_actions.md).

Sets the fall distance of the entity to the specified amount. The fall distance value keeps track of how many blocks the entity has fallen and is used to calculate the amount of fall damage the entity takes. By setting it to 0 while falling, the entity essentially takes fall damage as if it had only fallen from the current position.

Type ID: `origins:set_fall_distance`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`fall_distance` | [Float](../data_types/float.md) |  | The desired fall distance value.

### Example
```json
"entity_action": {
  "type": "origins:set_fall_distance",
  "fall_distance": 0
}
```
Resets the entity's fall distance so the fall damage is now calculated from that point.
