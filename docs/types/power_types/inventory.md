---
title: Inventory (Power Type)
date: 2021-04-08
---

# Inventory

[Power Type](../power_types.md)

Provides an inventory with 9 slots that can be opened with the specified [Key](../data_types/key.md); may or may not persist on death.

Type ID: `origins:inventory`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`title` | [String](../data_types/string.md) | `"container.inventory"` | The translation key or literal text to use as the display name for the inventory.
`container_type` | [Container Type](../../misc/extras/container_type.md) | `"dropper"` | Determines what type of container the inventory will be similar to.
`drop_on_death` | [Boolean](../data_types/boolean.md) | `false` | When this is set to true, the player will drop the items in the inventory on death (vanishing items will vanish!).
`drop_on_death_filter` | [Item Condition Type](../item_condition_types.md) | _optional_ | If this is set, only item stacks matching this condition will be dropped on death.
`recoverable` | [Boolean](../data_types/boolean.md) | `true` | Determines if the content of the inventory should be dropped upon losing the power.
`key` | [Key](../data_types/key.md) | _optional_ | Which active key this power should respond to. If none is specified, this power will use the primary active power key (by default G).


### Examples

```json
{
	"type": "origins:inventory",
	"container_type": "hopper",
	"drop_on_death": false,
	"key": {
		"key": "key.hotbar.9"
	}
}
```

This example will allow the player to open an inventory similar to a Hopper; consisting only of 5 slots but does not drop on death.
<br>

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

This example will allow the player to open a 9-slots inventory of which only non-food items will drop on death.
