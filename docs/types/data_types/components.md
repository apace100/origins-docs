---
title: Components (Data Type)
date: 2026-04-13
---

# Components

[Data Type](../data_types.md)

An [object](object.md) used to store information and define certain behavior. Mostly used by items (and referred as "item components" or "item stack components") and partially implemented for block entities.

!!! info

    See [Minecraft Wiki: Data component format (List of components)](https://minecraft.wiki/w/Data_component_format#List_of_components) for a list of component types used in items.

### Examples

```json
"components": {
    "minecraft:custom_name": "{\"text\": \"Mysterious Item\", \"italic\": false}"
}
```
This example represents a component with the [`minecraft:custom_name`](https://minecraft.wiki/w/Data_component_format#custom_name) component type, which defines the displayed name of an item.
<br>

```json
"components": {
    "minecraft:potion_contents": {
        "potion": "minecraft:water"
    },
    "minecraft:rarity": "epic"
}
```
This example represents a component with the [`minecraft:potion_contents`](https://minecraft.wiki/w/Data_component_format#potion_contents) and the [`minecraft:rarity`](https://minecraft.wiki/w/Data_component_format#rarity) component types, which defines the applied potion effects (when an item is consumed) and the color of the name of an item.
