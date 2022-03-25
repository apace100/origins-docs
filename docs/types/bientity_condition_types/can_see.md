---
title: Can See (Bi-entity Condition Type)
date: 2021-10-06
---

# Can See

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks whether the straight path from the actor entity's eyes to the target entity's eyes is unobstructed.

Type ID: `apoli:can_see`

### Fields

| Field            | Type                                              | Default    | Description                                     |
| ---------------- | ------------------------------------------------- | ---------- | ----------------------------------------------- |
| `shape_type`     | [Shape Type](../data_types/shape_type.md)         | `"visual"` | Determines how the ray-cast will handle blocks. |
| `fluid_handling` | [Fluid Handling](../data_types/fluid_handling.md) | `"none"`   | Determines how the ray-cast will handle fluids. |

### Examples

```json
"bientity_condition": {
    "type": "apoli:can_see"
}
```

This example will check if the straight path from the actor entity's eyes to the target entity's eyes is unobstructed. If the actor/target is behind a source/flowing fluid, is submerged in any kind of fluids, or behind a block that is not see-through (like Glass), the condition will return false.
