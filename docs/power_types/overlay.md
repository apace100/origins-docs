---
title: Overlay (Power Type)
date: 2021-10-02
---
# Overlay

[Power Type](../power_types.md)

Applies an overlay to the player's screen

Type ID: `origins:overlay`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`texture` | [Identifier](../data_types/identifier.md) | | The ID of the texture to use as an overlay.
`strength` | [Float](../data_types/float.md) | 1.0 | Value by which the alpha (transparency) component of the texture will be multiplied. Range: 0.0 to 1.0.
`red` | [Float](../data_types/float.md) | 1.0 | Value by which the red component of the texture will be multiplied. Range: 0.0 to 1.0.
`green` | [Float](../data_types/float.md) | 1.0 | Value by which the green component of the texture will be multiplied. Range: 0.0 to 1.0.
`blue` | [Float](../data_types/float.md) | 1.0 | Value by which the blue component of the texture will be multiplied. Range: 0.0 to 1.0.
`draw_mode` | [String](../data_types/string.md) | | Determines whether to use the Nausea overlay, or a custom texture defined by the `texture` field. Accepts either `"nausea"` or `"texture"`
`draw_phase` | [String](../data_types/string.md) | | Determines if the overlay should render below or above the HUD. Accepts either `"above_hud"` or `"below_hud"`.
`hide_with_hud` | [Boolean](../data_types/boolean.md) | true | Determines if the overlay should be hidden if the HUD elements are hidden (with F1).
`visible_in_third_person` | [Boolean](../data_types/boolean.md) | false | Determines if the overlay is visible in third person.

### Example
```json
{
    "type": "origins:overlay",
    "texture": "minecraft:textures/block/ice.png",
    "strength": 1.0,
    "red": 1.0,
    "green": 1.0,
    "blue": 1.0,
    "draw_mode": "texture",
    "draw_phase": "below_hud",
    "hide_with_hud": false,
    "visible_in_third_person": false
}
```
This example will render an overlay with the texture of an Ice block, below the HUD and is not visible in third person.