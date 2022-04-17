---
title: Prevent Feature Render
date: 2021-12-04
---

# Prevent Feature Render

[Power Type](../power_types.md)

Prevents certain [feature renderers](../../misc/extras/feature_renderers.md) (like the wool coat of a Sheep, the worn armor of a mob, etc.) from rendering on the entity that has the power.

Type ID: `origins:prevent_feature_render`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`feature` | [Feature Renderer](../../misc/extras/feature_renderers.md) | _optional_ | If specified, this feature renderer will not be rendered.
`features` | [Array](../data_types/array.md) of [Feature Renderers](../../misc/extras/feature_renderers.md) | _optional_ | If specified, these feature renderers will not be rendered.


### Examples

```json
{
    "type": "origins:prevent_feature_render",
    "features": [
        "armor",
        "held_item",
        "elytra"
    ]
}
```

This example will make the worn armor, held item and worn Elytra disappear as if the entity that has the power isn't wearing or holding an item.
