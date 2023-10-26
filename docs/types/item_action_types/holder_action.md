---
title: Holder Action (Item Action Type)
date: 2023-10-26
---


#	Holder Action

[Item Action Type](../item_action_types.md)

Executes an entity action on the holder of the item stack.

Type ID: `origins:holder_action`

Aliases: `origins:holder`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`action` | [Entity Action Type](../entity_action_types.md) | *optional* | The entity action to execute on the holder of the item stack.
`entity_action` | [Entity Action Type](../entity_action_types.md) | *optional* | The same as the `action` field, but with a different name.


###	Examples

```json
"item_action": {
	"type": "origins:holder_action",
	"action": {
		"type": "apoli:heal",
		"amount": 4.0
	}
}
```

This example will recover 2 hearts (4 health points) of the holder of the item stack.
