---
title: Resource (Power Type)
date: 2021-04-08
---

# Resource

[Power Type](../power_types.md)

Provides a variable with an assignable minimum and maximum value that can be used as a timer, or other things.

Type ID: `origins:resource`

!!! note

    This power type provides a variable that can be changed with the [Change Resource](../entity_actions/change_resource.md) entity action type, and check the value of with the [Resource](../entity_conditions/resource.md) entity condition type.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`min` | [Integer](../types/data_types/integer.md) | | The minimum value of the resource.
`max` | [Integer](../types/data_types/integer.md) | | The maximum value of the resource.
`hud_render` | [Hud Render](../types/data_types/hud_render.md) | | Determines how the resource is visualized on the HUD.
`start_value` | [Integer](../types/data_types/integer.md) | _optional_ | The value of the resource when the entity first receives the power. If not set, this will be set to the value of the `min` integer field.
`min_action` | [Entity Action](../entity_actions.md) | _optional_ | If specified, this action will be executed on the entity whenever the minimum value is reached.
`max_action` | [Entity Action](../entity_actions.md) | _optional_ | If specified, this action will be executed on the entity whenever the maximum value is reached.

### Example
```json
{
    "type": "origins:resource",
    "min": 0,
	"max": 1,
	"hud_render": {
		"should_render": false
	}
}
```
This power is a resource which stores a value of either 0 or 1, effectively being able to act as a toggle or boolean which can be changed from entity actions.
