---
title: Cooldown (Power Type)
date: 2021-04-07
---
# Cooldown

[Power Type](../power_types.md).

A generic power with a cooldown. The cooldown can be started with the [Trigger Cooldown](../entity_actions/trigger_cooldown.md) action. You can check whether the cooldown has passed with a [Resource](../entity_conditions/resource.md) condition checking for the value of the cooldown power to be 0.

Type ID: `origins:cooldown`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](../data_types/integer.md) | | Cooldown duration in ticks.
`hud_render` | [Hud Render](../data_types/hud_render.md) | | Specifies how and if a cooldown bar is rendered.


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