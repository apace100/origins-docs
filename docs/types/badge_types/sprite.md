---
title: Sprite (Badge Type)
date: 2022-07-03
---

#   Sprite

[Badge Type](../badge_types.md)

Displays a texture next to the name of the power.

Type ID: `origins:sprite`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`sprite` | [Identifier](../identifier.md) | | The namespace, path and ID of the texture to use as the icon of the badge.


### Examples

```json
{
    "type": "origins:sprite",
    "sprite": "origins:textures/gui/badge/arrow_up.png"
}
```

This example will display the [`origins:textures/gui/badge/arrow_up.png`](https://github.com/apace100/origins-fabric/blob/1.19/src/main/resources/assets/origins/textures/gui/badge/arrow_up.png) texture.
