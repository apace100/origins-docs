---
title: Modify Harvest (Power Type)
date: 2021-04-06
---

# Modify Harvest

[Power Type](../power_types.md)

Modifies whether a player is able to harvest a block or not (= receive the block drops).

Type ID: `apoli:modify_harvest`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If set, the modification will only apply to blocks which satisfy this condition.
`allow` | [Boolean](../data_types/boolean.md) | _optional_ | When true, the player will be able to harvest the blocks. When false, the player will not be able to harvest the blocks.



### Examples

```json
{
    "type": "apoli:modify_harvest",
    "block_condition": {
        "type": "apoli:block",
        "block": "minecraft:diamond_block"
    },
    "allow": true
}
```

This example will allow players to harvest a Diamond Block regardless of using the proper tool or not.
