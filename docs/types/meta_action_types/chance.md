---
title: Chance (Meta Action Type)
date: 2021-04-07
---

# Chance

[Meta Action Type](../meta_action_types.md)

Executes the provided action only with a specific chance.

Type ID: `origins:chance`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Action](../action_types.md) | | The action which might be executed.
`chance` | [Float](../data_types/float.md) | | The chance that the action will execute, from 0 to 1. (E.g. 0.1 means 10% chance, 0.95 means 95% chance).
`fail_action` | [Action](../action_types.md)| *optional* | The action to execute if the specified action in the `action` field is not executed.


### Examples

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

This example has a 40% chance to set the entity on fire for 5 seconds.
