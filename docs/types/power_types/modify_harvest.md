---
title: Modify Harvest (Power Type)
date: 2021-04-06
---

# Modify Harvest

[Power Type](../power_types.md)

Modifies whether a player is able to harvest a block or not (= receive the block drops).

Type ID: `origins:modify_harvest`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, only blocks that fulfill this condition are affected.
`allow` | [Boolean](../data_types/boolean.md) | | Determines whether the player is be able to harvest the block.


### Examples

```json
{
    "type": "origins:modify_harvest",
    "block_condition": {
        "type": "origins:block",
        "block": "minecraft:diamond_block"
    },
    "allow": true
}
```

This example will allow players to harvest a Diamond Block regardless of using the proper tool or not.
