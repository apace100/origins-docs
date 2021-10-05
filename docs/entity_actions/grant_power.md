---
title: Grant Power (Entity Action)
date: 2021-10-05
---
# Grant Power

[Entity Action](../entity_actions.md)

Grants a power to the entity.

Type ID: `origins:grant_power`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The ID of the power to be granted to the entity.
`source` | [String](../data_types/string.md) | | The source of the power.

### Example
```json
"entity_action": {
    "type": "origins:grant_power",
    "power": "origins:burn_in_daylight",
    "source": "example:power_source"
}
```
This example grants the entity the `origins:burn_in_daylight` power from the `example:power_source` source.