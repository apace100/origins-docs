---
title: Ingredient (Data Type)
date: 2021-04-04
---

# Ingredient

[Data Type](../data_types.md)

_Either_: an [Object](object.md) specifying a registered item or item tag.

_Or_: an [Array](array.md) of [Objects](object.md) specifying a registered item or item tag.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item` | [Identifier](identifier.md) | _optional_ | ID of a registered item.
`tag` | [Identifier](identifier.md) | _optional_  | ID of an item tag. Will be ignored if `item` is set.


### Examples

```json
"ingredient": {
    "item": "minecraft:diamond"
}
```

An ingredient which matches a diamond.
<br>

```json
"ingredient": {
    "tag": "minecraft:wool"
}
```

An ingredient which matches any wool block.
<br>


```json
"ingredient": [
    {
        "item": "minecraft:cod"
    },
    {
        "item": "minecraft:cooked_cod"
    },
    {
        "tag": "minecraft:planks"
    }
]
```

An ingredient which matches cod in its raw or cooked form, or any of the wooden planks.