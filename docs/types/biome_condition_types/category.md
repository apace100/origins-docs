---
title: Category (Biome Condition Type)
date: 2021-04-05
---

# Category

[Biome Condition Type](../biome_condition_types.md)

Checks for the category of a biome.

Type ID: `origins:category`


!!! danger

    This biome condition type has been <span style="color:darkred"><b>removed</b></span> in Origins 1.13.0 due to the removal of biome categories in 1.18.2. 
    
    **Please use [In Tag (Biome Condition Type)](in_tag.md) instead**.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`category` | [Biome Category](../../misc/extras/biome_categories.md) | |  Which category the biome must be in order to succeed the check.


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
