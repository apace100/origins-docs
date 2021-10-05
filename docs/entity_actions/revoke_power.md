---
title: Revoke Power (Entity Action)
date: 2021-10-05
---
# Revoke Power

[Entity Action](../entity_actions.md)

Revokes a power from the entity from a specific power source.

Type ID: `origins:revoke_power`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The ID of the power to be revoked from the entity.
`source` | [String](../data_types/string.md) | | The source of the power.

### Example
```json
"entity_action": {
    "type": "origins:revoke_power",
    "power": "origins:elytra",
    "source": "origins:elytrian"
}
```
This example will revoke the `origins:elytra` power that's from the `origins:elytrian` source from the entity.