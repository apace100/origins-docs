---
title: Modify (Item Action Type)
date: 2021-10-02
---

# Modify

[Item Action Type](../item_action_types.md)

Applies an [item modifier](https://minecraft.fandom.com/wiki/Item_modifier) to the item stack.

Type ID: `apoli:modify`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`modifier` | [Identifier](../data_types/identifier.md) | | The ID of an item modifier.



### Examples

```json
"item_action": {
    "type": "apoli:modify",
    "modifier": "example:add_lore"
}
```

This example will apply the `test:add_lore` (`data/test/item_modifiers/add_lore.json`) item modifier to the item stack.
<br>

```json
{
    "function": "minecraft:set_lore",
    "entity": "this",
    "lore": [
        {
            "text": "Hello, I'm a custom lore line for your item :]",
            "color": "light_purple",
            "italic": false
        }
    ]
}
```

This being the contents of the `test:add_lore` (`data/test/item_modifiers/add_lore.json`) item modifier.
