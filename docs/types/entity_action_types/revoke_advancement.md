---
title: Revoke Advancement (Entity Action Type)
date: 2023-05-21
---

# Revoke Advancement

[Entity Action Type](../entity_action_types.md)

Revokes an advancement from the player.

Type ID: `origins:revoke_advancement`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`advancement` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the advancement to be revoked from the player.


### Examples

```json
"entity_action": {
    "type": "origins:revoke_advancement",
    "advancement": "minecraft:adventure/arbalistic"
}
```

This example will revoke the Arbalistic advancement from the player, if they have it.
