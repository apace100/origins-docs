---
title: Delay (Meta Action Type)
date: 2021-04-07
---

# Delay

[Meta Action Type](../meta_action_types.md)

Executes the provided action after a set amount of ticks.

Type ID: `origins:delay`

!!! caution

    Delaying an action for more than a few ticks is not recommended! This meta action type is not reliable for such a task.

    If you want to delay an action type *reliably,* you can use a power that would use the [Cooldown (Power Type)](../power_types/cooldown.md) and trigger that power with the [Trigger Cooldown (Entity Action Type)](../entity_action_types/trigger_cooldown.md).

    You can then use another power that would use the [Action Over Time (Power Type)](../power_types/action_over_time.md) and check if the value of the power that would use the [Cooldown (Power Type)](../power_types/cooldown.md) is `"=="` to `0` using the [Resource (Entity Condition Type)](../entity_condition_types/resource.md).


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Action Type](../action_types.md) | | The action which will be executed after the delay.
`ticks` | [Integer](../data_types/integer.md) | | The amount of ticks until the action is executed.


### Examples

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
This example will apply a Speed II status effect after 1 second.
