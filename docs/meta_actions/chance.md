---
title: Chance (Action)
date: 2021-04-07
---
# Chance

[Meta Action](../meta_actions.md).

Executes the provided action only with a specific chance.

Type ID: `origins:chance`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Action](../actions.md) | | The action which might be executed.
`chance` | [Float](../data_types/float.md) | | The chance that the action will execute, from 0 to 1. (E.g. 0.1 means 10% chance, 0.95 means 95% chance)

### Example

```json
"entity_action": {
  "type": "origins:chance",
  "action": {
    "type": "origins:set_on_fire",
    "duration": 5
  },
  "chance": 0.4
}
```

This action has a 40% chance to set the player on fire for 5 seconds.
