---
title: Resource (Power Type)
date: 2021-04-08
---

# Resource

[Power Type](../power_types.md)

Provides a variable with an assignable minimum and maximum value that can be used as a timer, or other things.

Type ID: `origins:resource`

!!! note

    This power type provides a variable that can be changed with the [Change Resource (Entity Action Type)](../entity_action_types/change_resource.md), and check the value of with the [Resource (Entity Condition Type)](../entity_condition_types/resource.md).


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`min` | [Integer](../data_types/integer.md) | | The minimum value of the resource.
`max` | [Integer](../data_types/integer.md) | | The maximum value of the resource.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | Determines how the resource is visualized on the HUD.
`start_value` | [Integer](../data_types/integer.md) | _optional_ | The value of the resource when the entity first receives the power. If not set, this will be set to the value of the `min` integer field.
`min_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity whenever the minimum value is reached.
`max_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity whenever the maximum value is reached.


### Examples

```json
{
    "type": "origins:resource",
    "min": 0,
	"max": 1,
	"hud_render": {
		"should_render": false
	},
    "min_action": {
        "type": "origins:heal",
        "amount": 6
    }
}
```

This example will provide a variable with a minimum value of 0 and a maximum value of 1, which can effectively serve as a boolean that can be changed with the [Change Resource (Entity Action Type)](../entity_action_types/change_resource.md).
