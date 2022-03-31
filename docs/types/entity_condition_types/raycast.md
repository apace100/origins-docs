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
`distance` | [Float](../data_types/float.md) | | Determines the maximum distance the ray-cast will travel.
`block` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the ray-cast should include blocks.
`entity` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the ray-cast should include entities.
`shape_type` | [Shape Type](../../misc/extras/shape_type.md) | `"visual"` | Determines how the ray-cast will handle blocks.
`fluid_handling` | [Fluid Handling](../../misc/extras/fluid_handling.md) | `"none"` | Determines how the ray-cast will handle fluids.
`match_bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the entity condition type will check if this bi-entity condition type is fulfilled by either or both the 'actor' (the entity being checked by the entity condition type) and 'target' (entity that the ray-cast has gone through). If not, the entity will be ignored.
`hit_bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the entity condition type will check if this bi-entity condition type is fulfilled by either or both the 'actor' (the entity being checked by the entity condition type) and 'target' (the entity that has hit by the ray-cast).
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the entity condition type will check if the block that was hit by the ray-cast fulfills this block condition type.


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

This example will check if a wolf mob is tamed by the entity that has fired the raycast. The raycast will ignore tamable mobs other than wolves.
