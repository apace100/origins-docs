---
title: Apply Effect (Action)
date: 2021-04-05
---
# Apply Effect

[Entity Action](../entity_actions.md).

Adds one or more status effects to the living entity. Does not have an effect on non-living entities.

Type ID: `origins:apply_effect`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Status Effect Instance](../data_types/status_effect_instance.md) | _optional_ | If set, this status effect will be applied by this action.
`effects` | [Array](../data_types/array.md) of [Status Effect Instances](../data_types/status_effect_instance.md) | _optional_ | If set, these status effects will be applied by this action.

### Example
```json
"entity_action": {
  "type": "origins:apply_effect",
  "effect": {
    "effect": "minecraft:speed",
    "duration": 400,
    "amplifier": 0
  }
}
```
This action applies a Speed I effect for 20 seconds to the entity.
