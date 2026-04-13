---
title: Item Stack (Data Type)
date: 2021-04-04
---
# Item Stack

[Data Type](../data_types.md)

An [object](object.md) which defines a stack of items.

### Fields

| Field        | Type                        | Default    | Description                       |
| --------------| -----------------------------| ------------| -----------------------------------|
| `id`         | [Identifier](identifier.md) |            | The ID of the registered item.    |
| `count`      | [Integer](integer.md)       | `1`        | The size of the item stack.       |
| `components` | [Components](components.md) | _optional_ | The components of the item stack. |


### Examples

```json
"stack": {
    "id": "minecraft:coal",
    "count": 24
}
```
This example defines a stack of 24 Coal items.
<br>

```json
"stack": {
    "id": "minecraft:golden_helmet",
    "components": {
        "minecraft:enchantments": {
            "minecraft:projectile_protection": 2
        }
    }
}
```
This example defines a stack of 1 Golden Helmet with Projectile Protection II enchantment.
