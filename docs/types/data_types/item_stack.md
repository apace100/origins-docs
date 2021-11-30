---
title: Item Stack (Data Type)
date: 2021-04-04
---

# Item Stack

[Data Type](../data_types.md)

An [Object](object.md) which defines a new item stack.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item` | [Identifier](identifier.md) | | ID of a registered item.
`amount` | [Integer](integer.md) | `1` | Size of the stack.
`tag` | [String](string.md) | _optional_ | NBT data of the item.


### Examples

```json
"stack": {
    "item": "minecraft:coal",
    "amount": 24
}
```

An item stack of 24 coal.
<br>

```json
"stack": {
    "item": "minecraft:golden_helmet",
    "tag": "{Enchantments: [{id: \"minecraft:projectile_protection\", lvl: 2s}]}"
}
```

An item stack of a golden helmet with Projectile Protection II.