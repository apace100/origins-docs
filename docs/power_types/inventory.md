---
title: Inventory (Power Type)
date: 2021-04-08
---
# Inventory

[Power Type](../power_types.md).

An active power which opens a 9-slot inventory which may or may not persist over deaths. Note that this power type does not accept conditions.

Type ID: `origins:inventory`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`name` | [String](../data_types/string.md) | "container.inventory" | The translation key or literal text to use as the display name for the inventory.
`drop_on_death` | [Boolean](../data_types/boolean.md) | false | When this is set to true, the player will drop the items in the inventory on death (vanishing items will vanish!).
`drop_on_death_filter` | [Item Condition](../item_conditions.md) | _optional_ | If this is set, only item stacks matching this condition will be dropped on death.
`key` | [Key](../data_types/key.md) | _optional_ | Which active key this power should respond to. If none is specified, this power will use the primary active power key (by default G).

### Example
```json
{
  	"type": "origins:inventory",
  	"drop_on_death": true,
	"drop_on_death_filter": {
		"type": "origins:food",
		"inverted": true
	}
}
```
This power allows the player to open a 9-slot inventory of which only non-food items will drop on death.
