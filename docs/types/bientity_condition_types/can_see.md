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
`shape_type` | [String](../data_types/string.md) | `"visual"` | Determines how the raycast will handle blocks. If set to `"visual"`, the raycast will only stop at blocks that are not see-through (like Glass, Tinted Glass, etc.). If set to `"collider"`, the raycast will only stop at blocks that are solid (cannot be walked through). If set to `"outline"`, the raycast will take the shape of the block into account.
`fluid_handling` | [String](../data_types/string.md) | `"none"` | Deterines how the raycast will handle fluids. If set to `"any"`, the raycast will stop at both flowing and source fluids. If set to `"source"`, the raycast will only stop at source fluids. If set to `"none"`, the raycast will not stop at either source or flowing fluids.


### Examples

```json
"bientity_condition": {
    "type": "origins:can_see"
}
```

This example will check if the straight path from the actor entity's eyes to the target entity's eyes is unobstructed. If the actor/target is behind a source/flowing fluid, is submerged in any kind of fluids, or behind a block that is not see-through (like Glass), the condition will return false.
