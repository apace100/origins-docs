---
title: Change Resource (Entity Action Type)
date: 2021-04-05
---

# Change Resource

[Entity Action Type](../entity_action_types.md)

Changes the value of a power that either uses the [Resource](../power_types/resource.md) power type, or has a built-in cooldown.

Type ID: `apoli:change_resource`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`resource` | [Identifier](../data_types/identifier.md) |  | The namespace and ID of the power that uses the [Resource (Power Type)](../power_types/resource.md) or has a built-in cooldown.
`change` | [Integer](../data_types/integer.md) |  | This value will be added to the resource (won't go below `min` or above `max` of the [Resource (Power Type)](../power_types/resource.md)).
`operation` | [String](../data_types/string.md) | `"add"` | Determines if the action should add or set the value of the resource. Accepts `"add"` or `"set"`.


### Examples

```json
"entity_action": {
    "type": "apoli:change_resource",
    "resource": "test:example_resource",
    "change": 1
}
```

This example will add 1 to the `test:example_resource` (`data/test/powers/example_resource.json`) power that uses the [Resource (Power Type)](../power_types/resource.md).