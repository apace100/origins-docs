---
title: Prevent Block Use (Power Type)
date: 2021-04-07
---

# Prevent Block Use

[Power Type](../power_types.md)

Prevents the usage of blocks for the player that has the power.

Type ID: `origins:prevent_block_use`

!!! note

    Preventing the "usage" of a block means that the player won't be able to interact (right-click) with the said block.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | | If specified, only blocks that fulfill this condition are affected.


### Examples

```json
{
    "type": "origins:prevent_block_use",
    "block_condition": {
      "type": "origins:block",
      "block": "minecraft:crafting_table"
    }
}
```

This example will prevent the player from using Crafting Tables.
