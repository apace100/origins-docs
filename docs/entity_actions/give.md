---
title: Give (Action)
date: 2021-04-06
---
# Give

[Entity Action](../entity_actions.md).

Gives the entity an item stack, by inserting it into its inventory or dropping it on the ground if there is no available space.

Type ID: `origins:give`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`stack` | [Item Stack](../data_types/item_stack.md) |  | The item stack to give to the entity.

### Example
```json
"entity_action": {
  	"type": "origins:give",
  	"stack": {
	  "item": "minecraft:egg",
	  "amount": 3
  	}
}
```
Gives the entity a stack of 3 eggs.
