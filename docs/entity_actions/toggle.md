---
title: Toggle (Entity Action)
date: 2021-10-03
---
# Toggle

[Entity Action](../entity_actions.md)

Toggles the state of a power that uses the [`origins:toggle`](../power_types/toggle.md) power type.

Type ID: `origins:toggle`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power that uses the `origins:toggle` power type.

### Example
```json
"entity_action": {
    "type": "origins:toggle",
    "power": "origins:phantomize"
}
```
This example will toggle the [`origins:phantomize`](https://github.com/apace100/origins-fabric/blob/1.17/src/main/resources/data/origins/powers/phantomize.json) (`data/origins/powers/phantomize.json`) power if executed.