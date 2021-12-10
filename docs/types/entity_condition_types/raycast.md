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
`shape_type` | [String](../data_types/string.md) | `"outline"` | Determines how the raycast handles blocks. If set to `"outline"`, the raycast will take the shape of the collision box of the block into account. If set to `"visual"`, the raycast will ignore blocks that are see-through (e.g: Glass, Tinted Glass, etc.). If set to `"collider"`, the raycast will take physical collision of the block into account.
`fluid_handling` | [String](../data_types/string.md) | `"any"` | Determines how the raycast handles fluids. If set to `"any"`, the raycast will ignore source and flowing fluids. If set to `"source"`, the raycast will only go through source fluids. If set to `"none"`, the raycast **won't** go through any kind of fluids.
`match_bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the entity condition type will check if this bi-entity condition type is fulfilled by the entity that the raycast has gone through. If not, the entity will be ignored.
`hit_bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the entity condition type will check if the entity that was hit by the raycast fulfills this bi-entity condition type.
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the entity condition type will check if the block that was hit by the raycast fulfills this block condition type.


### Examples

```json
"condition": {
    "type": "origins:raycast",
    "distance": 6,
    "block": true,
    "entity": false,
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
