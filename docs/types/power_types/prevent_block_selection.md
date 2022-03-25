---
title: Prevent Block Selection (Power Type)
date: 2021-04-07
---

# Prevent Block Selection

[Power Type](../power_types.md)

Prevents the selection (i.e. targetting) of blocks for a player. This means they are not able to mine them, and attacks, interactions, etc. will pass through the block to whatever's behind it.

Type ID: `apoli:prevent_block_selection`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, only blocks that fulfills this condition is affected.


### Examples

```json
{
    "type": "apoli:prevent_block_selection",
    "block_condition": {
      "type": "apoli:block",
      "block": "minecraft:cobweb"
    },
    "condition": {
      "type": "apoli:sneaking",
      "inverted": true
    }
}
```

This example will prevent the selection of cobweb blocks, allowing the player to punch through them, unless they sneak.
