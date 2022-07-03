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
    "resource": "example:resource/a"
}
```

This example will add 1 to the `example:resource/a` power.
<br>

```json
"entity_action": {
    "type": "origins:modify_resource",
    "modifier": {
        "operation": "set_total",
        "resource": "example:resource/b"
    },
    "resource": "example:resource/a"
}
```

This example will use the value of the `example:resource/b` power as the value for the `example:resource/a` power.
