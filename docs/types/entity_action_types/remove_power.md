---
title: Remove Power (Entity Action Type)
date: 2023-10-26
---


#	Remove Power

[Entity Action Type](../entity_action_types.md)

Removes a power from the entity, regardless of its source.

Type ID: `origins:remove_power`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | [Identifier](../data_types/identifier.md) | | The ID of the power to remove from the entity.


###	Examples

```json
"entity_action": {
	"type": "origins:remove_power",
	"power": "origins:arcane_skin"
}
```

This example will remove the `origins:arcane_skin` power from the entity.
<br>


```json
"entity_action": {
	"type": "origins:remove_power",
	"power": "*:*"
}
```

This example will remove the power itself from the entity.
