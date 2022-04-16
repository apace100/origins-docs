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
`distance` | [Float](../data_types/float.md) | | Determines the maximum distance the ray-cast will travel.
`block` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the ray-cast should include blocks.
`entity` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the ray-cast should include entities.
`shape_type` | [Shape Type](../../misc/extras/shape_types.md) | `"visual"` | Determines how the ray-cast will handle blocks.
`fluid_handling` | [Fluid Handling](../../misc/extras/fluid_handling.md) | `"none"` | Determines how the ray-cast will handle fluids.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified bi-entity action type will only be executed if the specified bi-entity condition type is fulfilled by either or both the 'actor' (the entity that has the power) or 'target' (the entity that was hit by the ray-cast).
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this bi-entity action type will be executed on either or both the 'actor' (the entity that has the power) or 'target' (the entity that was hit by the ray-cast).
`block_action` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this block action type will be executed on the block the ray-cast has hit.
`before_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, execute this entity action type *before* casting a ray.
`hit_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, execute this entity action on the entity that executed the ray-cast if the ray-cast has hit an entity/block.
`miss_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, execute this entity action on the entity that executed the ray-cast if the ray-cast did not hit an entity/block.
`command_at_hit` | [String](../data_types/string.md) | _optional_ | The command to execute upon the block/entity the ray-cast has hit.
`command_hit_offset` | [Float](../data_types/float.md) | _optional_ | Determines the offset of the command specified in the `command_at_hit` field.
`command_along_ray` | [String](../data_types/string.md) | _optional_ | The command to execute for each step of the ray-cast.
`command_step` | [Float](../data_types/float.md) | `1.0` | Determines the size of the step of the ray-cast.
`command_along_ray_only_on_hit` | [Boolean](../data_types/boolean.md) | `false` | Determines if the command specified in the `command_along_ray` field should be executed only if the ray-cast has hit a block/entity.


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
