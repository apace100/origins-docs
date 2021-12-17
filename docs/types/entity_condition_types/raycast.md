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
`distance` | [Float](../data_types/float.md) | | Determines the maximum distance the raycast will travel.
`block` | [Boolean](../data_types/boolean.md) | `true` | If set to `false`, the raycast will ignore blocks.
`entity` | [Boolean](../data_types/boolean.md) | `true` | If set to `false`, the raycast will ignore entities.
`shape_type` | [String](../data_types/string.md) | `"visual"` | Determines how the raycast will handle blocks. If set to `"visual"`, the raycast will only stop at blocks that are not see-through (like Glass, Tinted Glass, etc.). If set to `"collider"`, the raycast will only stop at blocks that are solid (cannot be walked through). If set to `"outline"`, the raycast will take the shape of the block into account.
`fluid_handling` | [String](../data_types/string.md) | `"none"` | Deterines how the raycast will handle fluids. If set to `"any"`, the raycast will stop at both flowing and source fluids. If set to `"source"`, the raycast will only stop at source fluids. If set to `"none"`, the raycast will not stop at either source or flowing fluids.
`match_bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the entity condition type will check if this bi-entity condition type is fulfilled by either or both the 'actor' (the entity being checked by the entity condition type) and 'target' (entity that the raycast has gone through). If not, the entity will be ignored.
`hit_bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the entity condition type will check if this bi-entity condition type is fulfilled by either or both the 'actor' (the entity being checked by the entity condition type) and 'target' (the entity that has hit by the raycast).
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the entity condition type will check if the block that was hit by the raycast fulfills this block condition type.


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
