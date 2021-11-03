---
title: Status Bar Texture (Power Type)
date: 2021-10-02
---

# Status Bar Texture

[Power Type](../power_types.md)

Replaces the status bar textures (health, hunger, air, experience, etc.) with a specified sprite sheet.

Type ID: `origins:status_bar_texture`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`texture` | [Identifier](../data_types/identifier.md) | | The ID of the sprite sheet to replace the default one with. [Here's what the vanilla sprite sheet looks like.](https://media.discordapp.net/attachments/802622603008409600/893716345055772682/unknown.png)

### Example
```json
{
    "type": "origins:status_bar_texture",
    "texture": "example:textures/gui/custom_thing.png"
}
```
This example replaces the status bar textures with the `example:textures/gui/custom_thing.png` (`assets/example/textures/gui/custom_thing.png`) sprite sheet.