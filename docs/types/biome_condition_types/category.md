---
title: Category (Biome Condition Type)
date: 2021-04-05
---

# Category

[Biome Condition Type](../biome_condition_types.md)

Checks for the category of a biome.

Type ID: `origins:category`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`category` | [String](../data_types/string.md) | |  Which category the biome must be in order to succeed the check. See [List of Biome Categories](../../misc/extras/biome_categories.md) for possible values. 


### Examples

```json
"condition": {
    "type": "origins:biome",
    "condition": {
        "type": "origins:category",
        "category": "forest"
    }
}
```

This example will check if the player is inside a Forest-like biome.