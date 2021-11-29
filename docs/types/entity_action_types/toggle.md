---
title: Toggle (Entity Action Type)
date: 2021-10-03
---

# Toggle

[Entity Action Type](../entity_action_types.md)

Toggles the state of a power that uses the [Toggle (Power Type)](../power_types/toggle.md).

Type ID: `origins:toggle`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power that uses the [Toggle (Power Type)](../power_types/toggle.md).


### Examples

```json
"entity_action": {
    "type": "origins:toggle",
    "power": "origins:phantomize"
}
```

This example will toggle the state of the [`origins:phantomize`](https://github.com/apace100/origins-fabric/blob/1.17/src/main/resources/data/origins/powers/phantomize.json) (`data/origins/powers/phantomize.json`) power (e.g: ON --> OFF, OFF --> ON).