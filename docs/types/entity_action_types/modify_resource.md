---
title: Modify Resource (Entity Action Type)
date: 2022-07-03
---

#   Modify Resource

[Entity Action Type](../entity_action_types.md)

Modifies the value of a certain resource with [Attribute Modifiers](../data_types/attribute_modifier.md).

Type ID: `origins:modify_resource`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | | This modifier will be applied to the current value of the target power.
`resource` | [Identifier](../data_types/identifier.md) | | This power will have its value modified; as long as the power is using the [Resource (Power Type)](../power_types/resource.md) or the [Cooldown (Power Type)](../power_types/cooldown.md).


### Examples

```json
"entity_action": {
    "type": "origins:modify_resource",
    "modifier": {
        "operation": "add_base_early",
        "value": 1
    },
    "resource": "example:1st_resource"
}
```

This example will add 1 to the `example:1st_resource` *(`data/example/powers/1st_resource.json`)* power.
<br>

```json
"entity_action": {
    "type": "origins:modify_resource",
    "modifier": {
        "operation": "set_total",
        "value": 0,
        "resource": "example:2nd_resource"
    },
    "resource": "example:1st_resource"
}
```

This example will set the value of the `example:1st_resource` *(`data/example/powers/1st_resource.json`)* power as the value of the `example:2nd_resource` *(`data/example/powers/2nd_resource.json`)* power.
