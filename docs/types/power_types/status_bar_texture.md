---
title: Status Bar Texture (Power Type)
date: 2021-10-02
---

# Status Bar Texture

[Power Type](../power_types.md)

Replaces the status bar textures (health, hunger, air, experience, etc.) with a specified sprite sheet.

Type ID: `origins:status_bar_texture`


!!! note

    Custom status bar texture sprites are **required** to be placed within the `assets/.../textures/gui/sprites/hud` directory of a resource pack in order for the game to recognize and register properly.

    By extension, to reference status bar texture sprites in general, the `textures/gui/sprites` directory and the `.png` file extension **should** be omitted, as it's already implied.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`texture` | [Identifier](../data_types/identifier.md) | <span style="color: darkred"><b>DEPRECATED</b></span> | The identifier (including the `textures` directory and the `.png` file extension) of the status bar sprite sheet to replace teh default one with (e.g: [the vanilla status bar sprite sheet](https://raw.githubusercontent.com/misode/mcmeta/6d496b1a91476c4fdd45fdb093d0319141f9c109/assets/minecraft/textures/gui/icons.png)). <span style="color: darkred"><b>Use <code>texture_map</code> instead.</b></span>
`texture_map` | [Object](../data_types/object.md) | _optional_ | An object with `"key": "value"` [identifier](../data_types/identifier.md) pairs that determine which status bar texture sprite (`"key"`) will be replaced by a new status bar texture sprite (`"value"`). 


### Examples

```json
{
    "type": "origins:status_bar_texture",
    "texture": "example:textures/gui/custom_thing.png"
}
```

This example will replace the status bar textures with the `example:textures/gui/custom_thing.png` (`assets/example/textures/gui/custom_thing.png`) sprite sheet.
<br>

```json
{
    "type": "origins:status_bar_texture",
    "texture_map": {
        "minecraft:hud/heart/full": "example:hud/custom_heart/full",
        "minecraft:hud/heart/half": "example:hud/custom_heart/half"
    }
}
```

This example will replace the full (`assets/minecraft/textures/gui/sprites/hud/heart/full.png`), and half (`assets/minecraft/textures/gui/sprites/hud/heart/half.png`) heart status bar texture sprites with `example:hud/custom_heart/full` (`assets/example/textures/gui/sprites/hud/custom_heart/full.png`) and `example:hud/custom_heart/half` (`assets/example/textures/gui/sprites/hud/custom_heart/half.png`) custom status bar texture sprites respectively. 
