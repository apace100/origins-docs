---
title: Badge JSON
date: 2022-07-03
---

#   Badge JSON Format

This is the format of a JSON [Object](../types/data_types/object.md)/file describing a badge. A badge displays an icon after the name of a power in the power list of the Origins GUI screen.

Badge JSON files need to be placed inside the `data/<namespace>/badges` folder of your datapack. The said files can be referenced as `namespace:path/to/badge` (`data/namespace/badges/path/to/badge.json`) in the `badges` field of a [Power (JSON)](power.md) file.

Depending on the chosen `type`, badge JSONs have more required and optional fields. See the corresponding badge type page for a description of what those fields are.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`type` | [Badge Type](../types/badge_types.md) | `"origins:keybind"` | The namespace and ID of the desired badge type.


### Examples

```json
{
    "type": "origins:tooltip",
    "sprite": "origins:textures/gui/badge/star.png",
    "text": "A gold star!"
}
```

This example will display the [`origins:textures/gui/badge/star.png`](https://github.com/apace100/origins-fabric/blob/1.19/src/main/resources/assets/origins/textures/gui/badge/star.png) texture alongside a text that says "`A gold star!`"
