---
title: Prevent Block Use (Power Type)
date: 2021-04-07
---

# Prevent Block Use

[Power Type](../power_types.md)

Prevents the usage (i.e. right-clicking) of blocks for a player. For example, this could be used to make a player not able to open a furnace or chest, not use composters, or not use a button.

Type ID: `apoli:prevent_block_use`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | | If specified, only blocks that fulfills this condition is affected


### Examples

```json
{
    "type": "apoli:prevent_block_use",
    "block_condition": {
      "type": "apoli:block",
      "block": "minecraft:crafting_table"
    }
}
```

This example will prevent the player from using Crafting Tables.
