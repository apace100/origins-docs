---
title: Can See (Bi-entity Condition Type)
date: 2021-10-06
---

# Can See

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks whether the straight path from the actor entity's eyes to the target entity's eyes is unobstructed.

Type ID: `origins:can_see`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`shape_type` | [String](../data_types/string.md) | `"visual"` | Determines how the raycast handles blocks. If set to `"outline"`, the raycast will take the shape of the collision box of the block into account. If set to `"visual"`, the raycast will ignore blocks that are see-through (e.g: Glass, Tinted Glass, etc.). If set to `"collider"`, the raycast will take physical collision of the block into account.
`fluid_handling` | [String](../data_types/string.md) | `"none"` | Determines how the raycast handles fluids. If set to `"any"`, the raycast will ignore source and flowing fluids. If set to `"source"`, the raycast will only go through source fluids. If set to `"none"`, the raycast **won't** go through any kind of fluids.


### Examples

```json
"bientity_condition": {
    "type": "origins:can_see"
}
```

This example will check if the straight path from the actor entity's eyes to the target entity's eyes is unobstructed. If the actor/target is behind a source/flowing fluid, is submerged in any kind of fluids, or behind a block that is not see-through (like Glass), the condition will return false.
