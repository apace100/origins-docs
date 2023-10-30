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
`distance` | [Float](../data_types/float.md) | _optional_ | Determines the maximum distance the ray-cast will travel.
`block` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the ray-cast should include blocks.
`entity` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the ray-cast should include entities.
`shape_type` | [Shape Type](../data_types/shape_type.md) | `"visual"` | Determines how the ray-cast will handle blocks.
`fluid_handling` | [Fluid Handling](../data_types/fluid_handling.md) | `"any"` | Determines how the ray-cast will handle fluids.
`space` | [Space](../data_types/space.md) | _optional_ | The space to execute the raycast in. Defaults to "local" if no direction field is present. If a direction field is present, it will default to "world" instead.
`direction` | [Object](../data_types/object.md) | _optional_ | Used to specify the direction of the raycast. Can have a `x`, `y` and `z` [Floats](../data_types/float.md).
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified bi-entity action type will only be executed if the specified bi-entity condition type is fulfilled by either or both the 'actor' (the entity that has the power) or 'target' (the entity that was hit by the ray-cast).
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this bi-entity action type will be executed on either or both the 'actor' (the entity that has the power) or 'target' (the entity that was hit by the ray-cast).
`entity_distance` | [Float](../data_types/float.md) | _optional_ | Determines the distance of the raycast for entities if `entity` is set to `true`. If absent, it will use the higher value between the entity's attack range (with Reach Entity Attributes compatibility) or the `distance` field.
`block_action` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this block action type will be executed on the block the ray-cast has hit.
`block_distance` | [Float](../data_types/float.md) | _optional_ | Determines the distance of the raycast for blocks if `block` is set to `true`. If absent, it will use the higher value between the entity's block reach (with Reach Entity Attributes compatibility) or the `distance` field.
`before_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, execute this entity action type *before* casting a ray.
`hit_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, execute this entity action on the entity that executed the ray-cast if the ray-cast has hit an entity/block.
`miss_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, execute this entity action on the entity that executed the ray-cast if the ray-cast did not hit an entity/block.
`command_at_hit` | [String](../data_types/string.md) | _optional_ | The command to execute upon the block/entity the ray-cast has hit.
`command_hit_offset` | [Float](../data_types/float.md) | _optional_ | Determines the offset of the command specified in the `command_at_hit` field.
`command_along_ray` | [String](../data_types/string.md) | _optional_ | The command to execute for each step of the ray-cast.
`command_step` | [Float](../data_types/float.md) | `1.0` | Determines the size of the step of the ray-cast (in blocks).
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

```json
"entity_action": {
    "type": "origins:raycast",
    "block": true,
    "entity": true,
    "space": "local_horizontal_normalized",
    "direction": {
        "x": 0,
        "y": -0.5,
        "z": 1
    },
    "entity_distance": 2,
    "shape_type": "collider",
    "fluid_handling": "none",
    "bientity_action": {
        "type": "origins:target_action",
        "action": {
            "type": "origins:execute_command",
            "command": "say I've been hit!"
        }
    },
    "block_action": {
        "type": "apoli:execute_command",
        "command": "say A block has been hit"
    },
    "command_along_ray": "particle minecraft:soul_fire_flame"
}
```

This example will cast a ray that will travel in the direction that your body is facing towards but sligthly down, and will travel the same distance as your block reach for blocks, and two blocks for entities.
