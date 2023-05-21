---
title: Grant Advancement (Entity Action Type)
date: 2023-05-23
---

# Grant Advancement

[Entity Action Type](../entity_action_types.md)

Grants an advancement to the player.

Type ID: `origins:grant_advancement`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`advancement` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the advancement to be granted to the player.


### Examples

```json
"entity_action": {
    "type": "origins:grant_advancement",
    "advancement": "minecraft:adventure/arbalistic"
}
```

This example will grant the player the Arbalistic advancement.
