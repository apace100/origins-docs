---
title: Grant Power (Entity Action Type)
date: 2021-10-05
---

# Grant Power

[Entity Action Type](../entity_action_types.md)

Grants a power to the entity from a specified power source.

Type ID: `origins:grant_power`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power to be granted to the entity.
`source` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the source of the granted power.


### Examples

```json
"entity_action": {
    "type": "origins:grant_power",
    "power": "origins:burn_in_daylight",
    "source": "example:power_source"
}
```

This example will grant the entity the `origins:burn_in_daylight` power from the `example:power_source` source.
