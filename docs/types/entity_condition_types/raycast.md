---
title: Raycast (Entity Condition Type)
date: 2021-12-07
---

# Raycast

[Entity Condition Type](../entity_condition_types.md)

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
`space` | [Space](../data_types/space.md) | _optional_ | The space to execute the raycast in. Defaults to `"local"` unless `direction` has been specified, in which case it will default to `"world"`.
`direction` | [Object](../data_types/object.md) | _optional_ | Used to specify the direction of the raycast. Can have a `x`, `y` and `z` [Floats](../data_types/float.md).
`match_bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the entity condition type will check if this bi-entity condition type is fulfilled by either or both the 'actor' (the entity being checked by the entity condition type) and 'target' (entity that the ray-cast has gone through). If not, the entity will be ignored.
`hit_bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the entity condition type will check if this bi-entity condition type is fulfilled by either or both the 'actor' (the entity being checked by the entity condition type) and 'target' (the entity that has hit by the ray-cast).
`entity_distance` | [Float](../data_types/float.md) | _optional_ | Determines the distance of the raycast for entities if `entity` is set to `true`. If absent, it will use the higher value between the entity's attack range (with Reach Entity Attributes compatibility) or the `distance` field.
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the entity condition type will check if the block that was hit by the ray-cast fulfills this block condition type.
`block_distance` | [Float](../data_types/float.md) | _optional_ | Determines the distance of the raycast for blocks if `block` is set to `true`. If absent, it will use the higher value between the entity's block reach (with Reach Entity Attributes compatibility) or the `distance` field.


### Examples

```json
"condition": {
    "type": "origins:raycast",
    "distance": 6,
    "block": true,
    "entity": true,
    "shape_type": "visual",
    "fluid_handling": "any",
    "match_bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:wolf"
        }
    },
    "hit_bientity_condition": {
        "type": "origins:owner"
    }
}
```

This example will check if a wolf mob is tamed by the entity that has fired the ray-cast. The ray-cast will ignore tamable mobs other than wolves.
