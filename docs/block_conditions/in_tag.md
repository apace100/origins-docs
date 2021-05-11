---
title: In Tag (Condition)
date: 2021-04-05
---
# In Tag

[Block Condition](../block_conditions.md).

Checks whether the block is in a specified tag.

Type ID: `origins:in_tag`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`tag` | [String](../data_types/string.md) | | ID of the tag which the block should be in to pass the check.

### Example:
```json
"block_condition": {
    "type": "origins:in_tag",
    "tag": "minecraft:base_stone_overworld"
}
```
This example checks if the block is included in the `#minecraft:base_stone_overworld` (`data\minecraft\tags\blocks\base_stone_overworld.json`) block tag.