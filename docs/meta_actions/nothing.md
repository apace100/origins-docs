---
title: Nothing (Meta Action)
date: 2021-10-13
---
# Nothing

[Meta Action](../meta_actions.md)

Does nothing. Can be used as a backup in case an action is not optional in some place.

Type ID: `origins:nothing`

!!! note

    **Only available as an [Entity Action](../entity_actions.md) and a [Bi-entity Action](../bientity_actions.md)**

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