---
title: Category (Biome Condition Type)
date: 2021-04-05
---

# Category

[Biome Condition Type](../biome_condition_types.md)

Checks for the category of a biome.

Type ID: `origins:category`

!!! note

    [Click here for a list of biome categories.](../../misc/extra/biome_categories.md)

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`category` | [String](../data_types/string.md) | |  Which category the biome must be in order to succeed the check.

### Example:
```json
"condition": {
    "type": "origins:biome",
    "condition": {
        "type": "origins:category",
        "category": "forest"
    }
}
```
This example checks if the player is inside a Forest-like biome.