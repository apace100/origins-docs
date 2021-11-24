---
title: Equipped Item Action (Entity Action Type)
date: 2021-04-06
---

# Equipped Item Action

[Entity Action Type](../entity_action_types.md)

Executes an [Item Action](../item_actions.md) on an item stack in a specified equipment slot.

Type ID: `origins:equipped_item_action`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`equipment_slot` | [String](../data_types/string.md) | |  Which equipped item to execute the action on. One of: `"mainhand"`, `"offhand"`, `"head"`, `"chest"`, `"legs"`, `"feet"`.
`action` | [Item Action](../item_actions.md) | | The item action to execute.

### Example
```json
"entity_action": {
  	"type": "origins:equipped_item_action",
  	"equipment_slot": "mainhand",
  	"action": {
	  	"type": "origins:consume",
	  	"amount": 1
  	}
}
```
Removes 1 item from the stack in the entity's main hand.
