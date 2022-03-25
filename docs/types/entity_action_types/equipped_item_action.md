---
title: Equipped Item Action (Entity Action Type)
date: 2021-04-06
---

# Equipped Item Action

[Entity Action Type](../entity_action_types.md)

Executes an [Item Action Type](../item_action_types.md) on an item stack in a specified equipment slot.

Type ID: `apoli:equipped_item_action`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`equipment_slot` | [String](../data_types/string.md) | |  Which equipped item to execute the action on. One of: `"mainhand"`, `"offhand"`, `"head"`, `"chest"`, `"legs"`, `"feet"`.
`action` | [Item Action Type](../item_action_types.md) | | The item action type to execute on the item stack in the specified equipment slot.


### Examples

```json
"entity_action": {
  	"type": "apoli:equipped_item_action",
  	"equipment_slot": "mainhand",
  	"action": {
	  	"type": "apoli:consume",
	  	"amount": 1
  	}
}
```

This example will "consume" (remove) 1 item from the item stack in the mainhand equipment slot.
