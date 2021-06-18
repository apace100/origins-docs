---
title: Positioned Item Stack (Data Type)
date: 2021-04-04
---
# Positioned Item Stack

[Data Type](../data_types.md).

An [Object](object.md) which defines a new item stack alongside a position in an inventory. Basically an [Item Stack](item_stack.md) with a `slot` field.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`item` | [Identifier](identifier.md) | | ID of a registered item.
`amount` | [Integer](integer.md) | 1 | Size of the stack.
`tag` | [String](string.md) | _optional_ | NBT data of the item.
`slot` | [Integer](integer.md) | _optional_ | Inventory slot position of the stack. If not specified, will be the first free slot in the inventory. See [Positioned Item Stack Slots](../misc/positioned_item_stack_slots.md) for possible values

### Example:

```json
{
  	"stack": {
		"item": "minecraft:shield",
		"slot": 40
  	}
}
```

An item stack of a shield positioned in the off-hand slot of the player inventory.