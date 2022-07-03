---
title: Side (Meta Action Type)
date: 2022-06-15
---

#   Side

[Meta Action Type](../meta_action_types.md)

Executes the specified action type on the specified "side".


### Fields

Field | Type | Default | Description
------|------|---------|------------
`action` | [Action Type](../action_types.md) | | The action to execute.
`side` | [String](../data_types/string.md) | | Determines where to execute the specified action type. Accepts `"client"` or `"server"`


### Examples


```json
"entity_action": {
    "type": "origins:side",
    "action": {
        "type": "origins:change_resource",
        "resource": "example:resource",
        "change": 1
    },
    "side": "client"
}
```

This example will add 1 to the `example:resource` power on the client-side.
