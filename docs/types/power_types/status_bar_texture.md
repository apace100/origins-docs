---
title: Status Bar Texture (Power Type)
date: 2021-10-02
---

# Status Bar Texture

[Power Type](../power_types.md)

Replaces the status bar textures (health, hunger, air, experience, etc.) with a specified sprite sheet.

Type ID: `apoli:status_bar_texture`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`texture` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the sprite sheet to replace the default one with. [Here's what the vanilla sprite sheet looks like.](https://raw.githubusercontent.com/misode/mcmeta/6d496b1a91476c4fdd45fdb093d0319141f9c109/assets/minecraft/textures/gui/icons.png)


### Examples

```json
{
    "type": "apoli:status_bar_texture",
    "texture": "example:textures/gui/custom_thing.png"
}
```

This example will replace the status bar textures with the `example:textures/gui/custom_thing.png` (`assets/example/textures/gui/custom_thing.png`) sprite sheet.
