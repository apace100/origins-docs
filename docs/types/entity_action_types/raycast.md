---
title: Raycast (Entity Action Type)
date: 2021-12-04
---

# Raycast

[Entity Action Type](../entity_action_types.md)

Casts a ray to the direction where the entity is looking.

Type ID: `origins:raycast`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`distance` | [Float](../data_types/float.md) | | Determines the maximum distance the raycast will travel.
`block` | [Boolean](../data_types/boolean.md) | `true` | If set to `false`, the raycast will ignore blocks.
`entity` | [Boolean](../data_types/boolean.md) | `true` | If set to `false`, the raycast will ignore entities.
`shape_type` | [String](../data_types/string.md) | `"outline"` | Determines how the raycast handles blocks. If set to `"outline"`, the raycast will take the shape of the collision box of the block into account. If set to `"visual"`, the raycast will ignore blocks that are see-through (e.g: Glass, Tinted Glass). If set to `"collider"`, the raycast will take physical collision of the block into account.
`fluid_handling` | [String](../data_types/string.md) | `"any"` | Determines how the raycast should handle fluids. If set to `"any"`, the raycast will ignore source and flowing fluids. If set to `"source"`, the raycast will only go through source fluids. If set to `"none"`, the raycast **cannot** go through any kind of fluids.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified bi-entity action type will only be executed if the specified bi-entity condition type is fulfilled by either or both the 'actor' (the entity that has the power) or 'target' (the entity that was hit by the raycast).
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this bi-entity action type will be executed on either or both the 'actor' (the entity that has the power) or 'target' (the entity that was hit by the raycast).
`block_action` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this block action type will be executed on the block the raycast has hit.
`before_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, execute this entity action type *before* casting a ray.
`hit_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, execute this entity action type if the raycast has hit an entity/block.
`miss_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, execute this entity action type if the raycast did not hit an entity/block.
`command_at_hit` | [String](../data_types/string.md) | _optional_ | The command to execute upon the block/entity the raycast has hit.
`command_hit_offset` | [Float](../data_types/float.md) | _optional_ | Determines the offset of the command specified in the `command_at_hit` field.
`command_along_ray` | [String](../data_types/string.md) | _optional_ | The command to execute for each step of the raycast.
`command_step` | [Float](../data_types/float.md) | `1.0` | Determines the size of the step of the raycast.
`command_along_ray_only_on_hit` | [String](../data_types/string.md) | `false` | Determines if the command specified in the `command_along_ray` field should be executed only if the raycast has hit a block/entity.


### Examples

```json
"entity_action": {
    "type": "origins:raycast",
    "distance": 16,
    "block": true,
    "entity": true,
    "shape_type": "visual",
    "fluid_handling": "any",
    "bientity_action": {
        "type": "origins:target_action",
        "action": {
            "type": "origins:execute_command",
            "command": "say I've been hit!"
        }
    },
    "before_action": {
        "type": "origins:execute_command",
        "command": "say Before"
    },
    "hit_action": {
        "type": "origins:execute_command",
        "command": "say After (hit)"
    },
    "miss_action": {
        "type": "origins:execute_command",
        "command": "say After (miss)"
    },
    "command_at_hit": "particle minecraft:block_marker minecraft:emerald_block ~ ~ ~ 0 0 0 0.0 1 normal @a",
    "command_along_ray": "particle minecraft:soul_fire_flame",
    "command_step": 1,
    "command_along_ray_only_on_hit": true
}
```

This example will cast a ray that can go through Glass blocks (or any blocks that are transparent and see-through) that will only display the Soul Fire Flame particle if the ray has hit a block/entity.
