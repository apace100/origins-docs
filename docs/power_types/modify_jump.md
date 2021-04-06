---
title: Modify Jump (Power Type)
date: 2021-04-06
---
# Modify Jump

[Power Type](../power_types.md).

Modifies how high the player jumps.

Type ID: `origins:modify_jump`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If set, this modifier will apply to the upwards jump velocity.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, these modifiers will apply to the upwards jump velocity.
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will execute when the player jumps.
