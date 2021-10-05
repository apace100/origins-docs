---
title: Set Resource (Entity Action)
date: 2021-10-05
---
# Set Resource

[Entity Action](../entity_actions.md)

Sets the value of a [Resource (Power Type)](../power_types/resource.md)

Type ID: `origins:set_resource`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`resource` | [String](../data_types/string.md) | | The ID of the power that defines the resource.
`value` | [Integer](../data_types/integer.md) | | The value of the resource will be set with the specified value in this field.

### Example
```json
"entity_action": {
    "type": "origins:set_resource",
    "resource": "namespace:example",
    "set": 10
}
```
This example will set the value of the `namespace:example` (`data/namespace/powers/example.json`) power that uses the [`origins:resource`](../power_types/resource.md) power type.