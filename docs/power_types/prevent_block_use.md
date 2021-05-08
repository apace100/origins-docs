---
title: Prevent Block Use (Power Type)
date: 2021-04-07
---
# Prevent Block Use

[Power Type](../power_types.md).

Prevents the usage (i.e. right-clicking) of blocks for a player. For example, this could be used to make a player not able to open a furnace or chest, not use composters, or not use a button.

Type ID: `origins:prevent_block_use`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions.md) | | When set, only blocks which meet this condition will be unable to be used.

### Example
```json
{
    "type": "origins:prevent_block_use",
    "block_condition": {
      "type": "origins:block",
      "block": "minecraft:crafting_table"
    }
}
```
This power will prevent the player from using crafting tables.
