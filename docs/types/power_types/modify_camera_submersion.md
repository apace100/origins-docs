---
title: Modify Camera Submersion
date: 2021-10-03
---

# Modify Camera Submersion

[Power Type](../power_types.md)

Modifies how the player perceives the world, similarly to when they're submerged in fluids like water or lava.

Type ID: `apoli:modify_camera_submersion`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`from` | [String](../data_types/string.md) | _optional_ | Which submersion type to modify. Can be `none`, `water` or `lava`.
`to` | [String](../data_types/string.md) | _optional_ | Which submersion type to change to. Can be `none`, `water` or `lava`.


### Examples

```json
{
  "type": "apoli:modify_camera_submersion",
  "from": "none",
  "to": "water"
}
```

This example will make it look like the player is submerged in Water if the player is not submerged in any fluid.
