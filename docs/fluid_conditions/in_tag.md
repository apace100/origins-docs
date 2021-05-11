---
title: In Tag (Fluid Condition)
date: 2021-04-04
---
# In Tag

[Fluid Condition](../fluid_conditions.md).

Checks whether the fluid is in a specified tag.

Type ID: `origins:in_tag`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`tag` | [Identifier](../data_types/identifier.md) | |  ID of the tag which the fluid should be in to pass the check.

### Example:
```json
"fluid_condition": {
    "type": "origins:in_tag",
    "tag": "minecraft:water"
}
```
This example checks if the fluid is included in the `#minecraft:water` (`data\minecraft\tags\fluids`) block tag.