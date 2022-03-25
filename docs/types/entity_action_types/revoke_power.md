---
title: Revoke Power (Entity Action Type)
date: 2021-10-05
---

# Revoke Power

[Entity Action Type](../entity_action_types.md)

Revokes a power from the entity from a specified power source.

Type ID: `apoli:revoke_power`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power to be revoked from the entity.
`source` | [String](../data_types/string.md) | | The namespace and ID of the source of the power.


### Examples

```json
"entity_action": {
    "type": "apoli:revoke_power",
    "power": "test:example_power",
    "source": "example:test"
}
```

This example will revoke the `test:example_power` power that's from the `example:test` source from the entity.
