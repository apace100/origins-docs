---
title: Prevent Block Selection (Power Type)
date: 2021-04-07
---

# Prevent Block Selection

[Power Type](../power_types.md)

Prevents the selection (i.e. targetting) of blocks for a player. This means they are not able to mine them, and attacks, interactions, etc. will pass through the block to whatever's behind it.

Type ID: `origins:prevent_block_selection`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, only blocks that fulfil this condition are affected.


### Examples

```json
{
    "type": "origins:prevent_block_selection",
    "block_condition": {
      "type": "origins:in_tag",
      "tag": "origins:cobwebs"
    },
    "condition": {
      "type": "origins:sneaking",
      "inverted": true
    }
}
```

This example will prevent the selection of cobwebs (including the Temporary Cobweb block from the Arachnid's power), allowing the player to punch through them, unless they sneak.
