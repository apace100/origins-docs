---
title: Cooldown (Power Type)
date: 2021-04-07
---

# Cooldown

[Power Type](../power_types.md)

Provides a cooldown; can be used for providing cooldowns to power types that do not have a built-in cooldown.

Type ID: `origins:cooldown`

!!! note

    This power type provides a cooldown that can be triggered with the [Trigger Cooldown](../entity_actions/trigger_cooldown.md) and [Change Resource](../entity_actions/change_resource.md) entity action types, and check the value of with the [Resource](../entity_conditions/resource.md) entity condition type.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](../data_types/integer.md) | | Cooldown duration in ticks.
`hud_render` | [Hud Render](../data_types/hud_render.md) | | Determines how the cooldown of this power is visualized on the HUD.


### Example
```json
{
    "type": "origins:cooldown",
    "cooldown": 200,
    "hud_render": {
        "should_render": true,
        "bar_index": 3
    }
}
```
This power will last for 10 seconds (20 ticks = 1 second), and display the 4th resource bar sprite in the default sprite sheet if triggered with the [`origins:trigger_cooldown`](../entity_actions/trigger_cooldown.md) entity action.