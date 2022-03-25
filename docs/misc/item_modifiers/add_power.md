---
title: Add Power (Item Modifiers)
date: 2021-12-01
---

# Add Power

[Item Modifier](../item_modifiers.md)

Adds a power to an item stack that will only be applied to the player if the item is held/equipped in the specified equipment slot.

### Fields

| Field      | Type                                               | Default | Description                                                                                                                                                                   |
| ---------- | -------------------------------------------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `power`    | [Identifier](../../types/data_types/identifier.md) |         | The namespace and ID of the power that will be added to the entity.                                                                                                           |
| `slot`     | [String](../../types/data_types/string.md)         |         | Determines if the item should add the power to the entity if held/equipped in the specified equipment slot. Accepts `head`, `chest`, `legs`, `feet`, `mainhand` or `offhand`. |
| `hidden`   | [Boolean](../../types/data_types/boolean.md)       | `false` | Determines if the tooltip for the power should be hidden or not.                                                                                                              |
| `negative` | [Boolean](../../types/data_types/boolean.md)       | `false` | Determines if the color of the tooltip should be blue (false) or red (true).                                                                                                  |

### Examples

```json
{
	"function": "apoli:add_power",
	"power": "test:example_power",
	"slot": "chest",
	"negative": true
}
```

This example will add the `test:example_resource` (`data/test/powers/example_resource.json`) power to the entity if the entity were to wear the item that this item modifier has been applied to on their chest equipment slot.
