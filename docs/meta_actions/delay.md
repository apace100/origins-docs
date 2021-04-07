---
title: Delay (Action)
date: 2021-04-07
---
# Delay

[Meta Action](../meta_actions.md).

**Currently only available as an [Entity Action](../entity_actions.md)**

Executes the provided action after a set amount of ticks.

Type ID: `origins:delay`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Action](../actions.md) | | The action which will be executed after the delay.
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
