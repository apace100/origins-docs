---
title: Material (Block Condition Type)
date: 2021-12-09
---

# Material

[Block Condition Type](../block_condition_types.md)

Checks if the block is classified as the specified material.

Type ID: `origins:material`

!!! danger

    This block condition type has been <span style="color:darkred"><b>deprecated</b></span> and may be removed in a future version. Please use the [In Tag (Block Condition Type)](in_tag.md) instead.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`material` | [Material](../data_types/material.md) | _optional_ | If specified, checks if the block classifies as this material.
`materials` | [Array](../data_types/array.md) of [Materials](../data_types/material.md) | _optional_ | If specified, checks if the block classifies as one of these materials.


### Examples

```json
"block_condition": {
    "type": "origins:material",
    "material": "wood"
}
```

This example will check if the block classifies as "wood".
