---
title: NBT (Data Type)
date: 2023-07-07
---

#   NBT

[Data Type](../data_types.md)

A [string](string.md) or [object](object.md) that defines a named binary tag (NBT) for storing arbitrary data. It consists of key-value pairs (the key being the name of the tag) separated by a comma.


!!! note

    See [Minecraft Fandom Wiki: NBT format](https://minecraft.fandom.com/wiki/NBT_format) for more information about named binary tags (NBTs).


### Examples

```json
"nbt": "{example: {is_special: 1b, numbers: [100, 3, -56]}}"
```

This example defines an object NBT that contains an object NBT named `example`. The `example` object NBT then contains two NBTs: `is_special`, which is a byte NBT, and `numbers`, which is an integer array NBT.
<br>

```json
"nbt": {
    "example": {
        "is_special": 1b,
        "numbers": [
            100,
            3,
            -56
        ]
    }
}
```
This is the same example as above, but formatted as an actual object.
