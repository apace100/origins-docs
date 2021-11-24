---
title: Change Resource (Entity Action Type)
date: 2021-04-05
---

# Change Resource

[Entity Action Type](../entity_action_types.md)

Changes the value of a [Resource (Power Type)](../power_types/resource.md).

Type ID: `origins:change_resource`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`resource` | [Identifier](../data_types/identifier.md) |  | ID of the power type that defines the resource. Must be a [Resource (Power Type)](../power_types/resource.md) which exists on the player.
`change` | [Integer](../data_types/integer.md) |  | This value will be added to the resource (won't go below `min` or above `max` of the Resource [Resource (Power Type)](../power_types/resource.md)).
`operation` | [String](../data_types/string.md) | `"add"` | Determines if the action should add or set the value of the resource. Accepts `"add"` or `"set"`.

### Example
```json
"entity_action": {
    "type": "origins:change_resource",
    "resource": "namespace:example",
    "change": 1
}
```
This action adds 1 to the `namespace:example` [resource](../power_types/resource.md) power. (`data\namespace\powers\example.json`)