---
title: Resource (Power Type)
date: 2021-04-08
---
# Resource

[Power Type](../power_types.md).

Defines a resource/cooldown/timer for the player. Basically holds a persistent integer value which can be modified by the [Change Resource](../entity_actions/change_resource.md) action and checked with the [Resource (Condition)](../entity_conditions/resource.md) player condition.

Type ID: `origins:resource`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`min` | [Integer](../data_types/integer.md) | | The minimum value of the resource.
`max` | [Integer](../data_types/integer.md) | | The maximum value of the resource.
`hud_render` | [Hud Render](../data_types/hud_render.md) | | Specifies how and if the resource is displayed with a bar on the HUD.
`start_value` | [Integer](../data_types/integer.md) | _optional_ | The value of the resource when the player first chooses an origin with this power. If not set, this will be the same as `min`.
`min_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player whenever the minimum value is reached.
`max_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player whenever the maximum value is reached.

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
