---
title: Prevent Block Selection (Power Type)
date: 2021-04-07
---
# Prevent Block Selection

[Power Type](../power_types.md).

Prevents the selection (i.e. targetting) of blocks for a player. This means they are not able to mine them, and attacks, interactions, etc. will pass through the block to whatever's behind it.

Type ID: `origins:prevent_block_selection`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | When set, only blocks which meet this condition will be unable to be selected.

### Example
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
This power will prevent the selection of cobweb (the tag contains regular cobweb as well as the temporary cobweb from the Arachnid's power), allowing to punch through them, unless they sneak.
