---
title: Grant Power (Entity Action Type)
date: 2021-10-05
---

# Grant Power

[Entity Action Type](../entity_action_types.md)

Grants a power to the entity from a specified power source.

Type ID: `apoli:grant_power`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power to be granted to the entity.
`source` | [String](../data_types/string.md) | | The namespace and ID of the source of the granted power.


### Examples

```json
"entity_action": {
    "type": "apoli:grant_power",
    "power": "test:example_power",
    "source": "example:power_source"
}
```

This example will grant the entity the `test:example_power` power from the `example:power_source` source.