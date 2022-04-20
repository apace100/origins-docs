---
title: Relative Rotation (Bi-entity Condition Type)
date: 2021-12-04
---

# Relative Rotation

[Bi-entity Condition Type](../bientity_condition_types.md)

Compares the rotation angle of the 'actor' to the 'target'.

Type ID: `origins:relative_rotation`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`axes` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["x", "y", "z"]` | The axes to get the angle values to calculate, and compare to.
`actor_rotation` | [String](../data_types/string.md) | `"head"` | Determines the initial point of the rotation for the actor. Accepts `"head"` or `"body"`.
`target_rotation` | [String](../data_types/string.md) | `"body"` | Determines the initial point of the rotation for the target. Accepts `"head"` or `"body"`.
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the calculated angle value will be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value to compare the calculated angle value to.


### Examples

```json
"bientity_condition": {
    "type": "origins:relative_rotation",
    "actor_rotation": "head",
    "target_rotation": "body",
    "comparison": ">=",
    "compare_to": -0.8
}
```

This example will check if the actor and target are essentially facing each other.
<br>

```json
"bientity_condition": {
    "type": "origins:relative_rotation",
    "actor_rotation": "head",
    "target_rotation": "body",
    "comparison": ">=",
    "compare_to": 0.4
}
```

This example will check if the actor's head is essentially facing the same way as the target's body.
