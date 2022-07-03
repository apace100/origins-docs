---
title: Keybind (Badge Type)
date: 2022-07-03
---

#   Keybind

[Badge Type](../badge_types.md)

Displays a texture next to the name of the power and a tooltip with text upon being hovered with a Mouse cursor. `%s` will be translated to the keybind specified in the power.

Type ID: `origins:keybind`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`sprite` | [Identifier](../identifier.md) | | The namespace, path and ID of the texture to use as the icon of the badge.
`text` | [String](../string.md) | | The text to use in the tooltip.


### Examples

```json
{
    "type": "origins:keybind",
    "sprite": "origins:textures/gui/badge/toggle.png",
    "text": "Trigger with %s!"
}
```

This example will display the [`origins:textures/gui/badge/toggle.png`](https://github.com/apace100/origins-fabric/blob/1.19/src/main/resources/assets/origins/textures/gui/badge/toggle.png) texture alongside a text that says "`Trigger with <keybind>!`", where `<keybind>` is the name of the keybind specified in the power.
