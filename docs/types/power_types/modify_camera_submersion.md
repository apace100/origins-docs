---
title: Modify Camera Submersion
date: 2021-10-03
---

# Modify Camera Submersion

[Power Type](../power_types.md)

Modifies how the player perceives the world, similarly to when they're submerged in fluids like water or lava.

Type ID: `origins:modify_camera_submersion`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`from` | [String](../data_types/string.md) | _optional_ | If specified, only this submersion type will be modified. Accepts either `"none"` , `"water"` or `"lava"`
`to` | [String](../data_types/string.md) | | Which submersion type to change to. Accepts either `"none"`, `"water"` or `"lava"`


### Examples

```json
{
  "type": "origins:modify_camera_submersion",
  "from": "none",
  "to": "water"
}
```

This example will make it look like the player is submerged in Water if the player is not submerged in any fluid.
