---
title: Modify (Item Action Type)
date: 2021-10-02
---

# Modify

[Item Action Type](../item_action_types.md)

Applies an [Item Modifier](https://minecraft.wiki/w/Item_modifier) to the item stack.

Type ID: `origins:modify`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`modifier` | [Identifier](../data_types/identifier.md) | | The ID of an item modifier.



### Examples

```json
"item_action": {
    "type": "origins:modify",
    "modifier": "example:stuff"
}
```

This example will apply the `example:stuff` (`data/example/item_modifiers/stuff.json`) item modifier to the item stack.
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

This being the contents of the `example:stuff` (`data/example/item_modifiers/stuff.json`) item modifier.
