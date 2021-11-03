---
title: Badge (Data Type)
date: 2021-10-02
---

# Badge

[Data Type](../data_types.md)

An [Object](object.md) which displays an icon just after the name of a power in the power list from the Origins GUI.

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`sprite` | [Identifier](identifier.md) | | ID of the texture to be displayed as an icon.
`text` | [String](string.md) | | The string to display when you hover over the icon.

### Examples
```json
"badges": [
    {
        "sprite": "minecraft:textures/block/dirt.png",
        "text": "I'm a dirt badge!"
    }
]
```
This example displays a \[flat\] Dirt texture icon.
<br>

```json
"badges": [
    {
        "sprite": "origins:textures/gui/badge/star.png",
        "text": "Look mum, I have a star!"
    },
    {
        "sprite": "origins:textures/gui/badge/info.png",
        "text": "And yes, you can have multiple badges!"
    }
]
```
This example displays two badges: one that has a [star icon](https://github.com/apace100/origins-fabric/blob/1.17/src/main/resources/assets/origins/textures/gui/badge/star.png), and one that has an ['i' icon](https://github.com/apace100/origins-fabric/blob/1.17/src/main/resources/assets/origins/textures/gui/badge/info.png)