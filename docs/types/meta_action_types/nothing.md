---
title: Nothing (Meta Action Type)
date: 2021-10-13
---

# Nothing

[Meta Action Type](../meta_action_types.md)

Does nothing. Can be used as a backup in case an action is not optional in some place.

Type ID: `origins:nothing`

!!! note

    **Only available as an [Entity Action Type](../entity_action_types.md) and a [Bi-entity Action Type](../bientity_action_types.md).**


### Fields

_None._


### Examples

```json
"entity_action": {
    "type": "origins:nothing"
}
```

This example does.. nothing.
<br>

```json
"bientity_action": {
    "type": "origins:nothing"
}
```

This example also does.. nothing.
