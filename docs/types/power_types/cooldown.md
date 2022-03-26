---
title: Cooldown (Power Type)
date: 2021-04-07
---

# Cooldown

[Power Type](../power_types.md)

Provides a cooldown; can be used for providing cooldowns to power types that do not have a built-in cooldown or as a simple timer.

Type ID: `origins:cooldown`

!!! note

    This power type provides a cooldown that can be triggered with the [Trigger Cooldown (Entity Action Type)](../entity_action_types/trigger_cooldown.md) and [Change Resource (Entity Action Type)](../entity_action_types/change_resource.md), and check the value of with the [Resource (Entity Condition Type)](../entity_condition_types/resource.md).


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](../data_types/integer.md) | | Cooldown duration in ticks.
`hud_render` | [Hud Render](../data_types/hud_render.md) | | Determines how the cooldown of this power is visualized on the HUD.



### Examples

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

This example will provide a cooldown that will last for 10 seconds, and display the 4th resource bar sprite from the default sprite sheet.
