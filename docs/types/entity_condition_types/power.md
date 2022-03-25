---
title: Power (Entity Condition Type)
date: 2021-04-04
---

# Power

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity has a specified power.

Type ID: `apoli:power`

### Fields

| Field    | Type                                      | Default    | Description                                                                   |
| -------- | ----------------------------------------- | ---------- | ----------------------------------------------------------------------------- |
| `power`  | [Identifier](../data_types/identifier.md) |            | The namespace and ID of the power the entity needs to have to pass the check. |
| `source` | [Identifier](../data_types/identifier.md) | _optional_ | The namespace and ID of the source of the power.                              |

### Examples

```json
"condition": {
	"type": "apoli:power",
	"power": "test:example_power"
}
```

This example will check if the player has the `test:example_power`power.
