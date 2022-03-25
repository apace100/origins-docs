---
title: Modify Jump (Power Type)
date: 2021-04-06
---

# Modify Jump

[Power Type](../power_types.md)

Modifies how high the entity that has the power can jump.

Type ID: `apoli:modify_jump`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the upwards velocity.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the upwards velocity.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity that has the power whenever the entity jumps.



### Examples

```json
{
    "type": "apoli:modify_jump",
    "modifier": {
        "operation": "addition",
        "value": 0.4
    },
    "entity_action": {
        "type": "apoli:execute_command",
        "command": "particle cloud ~ ~ ~ 0.3 0.3 0.3 0.01 16 normal @a"
    }
}
```

This example will increase the entity that has the power's jump height to 4 blocks and display a cloud particle at the entity's feet upon jumping.
