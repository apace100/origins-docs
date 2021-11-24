---
title: Delay (Meta Action Type)
date: 2021-04-07
---

# Delay

[Meta Action Type](../meta_action_types.md)

Executes the provided action after a set amount of ticks.

Type ID: `origins:delay`

!!! note

    **Only available as an [Entity Action](../entity_actions.md)**

!!! caution

    Delaying an action for more than a few ticks is not recommended! This meta action type is not reliable for such task.

    If you want to delay an entity action *reliably,* you can use a power that uses the [`origins:resource`](../power_types/resource.md) power type and increase the value of that resource per set interval using a power that uses the [`origins:action_over_time`](../power_types/action_over_time.md) power type.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Entity Action](../entity_actions.md) | | The action which will be executed after the delay.
`ticks` | [Integer](../data_types/integer.md) | | The amount of ticks until the action is executed.

### Example

```json
"entity_action": {
    "type": "origins:delay",
    "ticks": 20,
    "action": {
        "type": "origins:apply_effect",
        "effect": {
            "effect": "minecraft:speed",
            "amplifier": 1,
            "duration": 80
        }
    }
}
```
This action will apply a speed effect after 1 second.
