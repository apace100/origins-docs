---
title: Modify Jump (Power Type)
date: 2021-04-06
---

# Modify Jump

[Power Type](../power_types.md)

Modifies how high the entity that has the power can jump.

Type ID: `origins:modify_jump`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../types/data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the upwards velocity.
`modifiers` | [Array](../types/data_types/array.md) of [Attribute Modifiers](../types/data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the upwards velocity.
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If specified, this action will be executed on the entity that has the power whenever the entity jumps.


### Example
```json
{
    "type": "origins:modify_jump",
    "modifier": {
        "operation": "addition",
        "value": 0.4
    },
    "entity_action": {
        "type": "origins:execute_command",
        "command": "particle cloud ~ ~ ~ 0.3 0.3 0.3 0.01 16 normal @a"
    }
}
```
This power modifies the player's jump height, increasing it to 4 blocks, and display a cloud particle at the player's feet.