---
title: Tooltip (Badge Type)
date: 2022-07-03
---

#   Tooltip

[Badge Type](../badge_types.md)

Displays a tooltip with text upon being hovered with a Mouse cursor.

Type ID: `origins:tooltip`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`sprite` | [Identifier](../identifier.md) | | The namespace, path and ID of the texture to use as the icon of the badge.
`text` | [Text Component](../data_types/text_component.md) | | The text to use in the tooltip.


### Examples

```json
{
    "type": "origins:tooltip",
    "sprite": "origins:textures/gui/badge/star.png",
    "text": "A gold star!"
}
```

This example will display the [`origins:textures/gui/badge/star.png`](https://github.com/apace100/origins-fabric/blob/1.19/src/main/resources/assets/origins/textures/gui/badge/star.png) texture alongside a text that says "`A gold star!`"
