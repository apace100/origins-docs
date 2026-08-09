---
title: Random Chance (Meta Action Type)
date: 2021-04-07
---

#   Random Chance

[Meta Action Type](../meta_action_types.md)

Executes the provided action only with a specific chance.

Type ID: [`origins:random_chance`](## "Previously "chance"")


### Fields

Field                                               |   Type                                |   Default     |   Description
----------------------------------------------------|---------------------------------------|---------------|--------------
[`success_action`](## "Previously "action"")        |   [Action Type](../action_types.md)   |               |   The action that will be executed if the roll succeeds.
`fail_action`                                       |   [Action Type](../action_types.md)   |   _optional_  |   If specified, this action will be executed if the roll fails.
`chance`                                            |   [Float](../data_types/float.md)     |               |   The chance that the action will execute, ranging from 0.0 to 1.0 (e.g: 0.1 means 10% chance, while 0.95 means 95% chance.)


### Examples

```json
"entity_action": {
    "type": "origins:random_chance",
    "success_action": {
        "type": "origins:set_on_fire",
        "duration": 5
    },
    "chance": 0.4
}
```
This example has a 40% chance to set the entity on fire for 5 seconds.
