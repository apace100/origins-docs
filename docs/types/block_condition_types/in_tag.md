---
title: In Tag (Block Condition Type)
date: 2021-04-05
---

# In Tag

[Block Condition Type](../block_condition_types.md)

Checks whether the block is in a specified tag.

Type ID: `origins:in_tag`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`tag` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the tag which the block should be in to pass the check.


### Examples

```json
"block_condition": {
    "type": "origins:in_tag",
    "tag": "minecraft:base_stone_overworld"
}
```

This example will check if the block is included in the `#minecraft:base_stone_overworld` (`data/minecraft/tags/blocks/base_stone_overworld.json`) block tag.
