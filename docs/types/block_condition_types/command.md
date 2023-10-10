---
title: Command (Block Condition Type)
date: 2023-10-09
---

# Command

[Block Condition Type](../block_condition_types.md)

Compares the result of the specified command to the specified value at the position of the block.

Type ID: `origins:command`

!!! caution

    This entity condition type only operates on the <span style="color:goldenrod"><b>server-side</b></span>, meaning that it cannot be used in fields that are evaluated on the client-side.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`command` | [String](../data_types/string.md) | |  The command to execute.
`comparison` | [Comparison](../data_types/comparison.md) | | How to compare the stored result of the specified command to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value to compare the stored result of the specified command to.


### Examples

```json
"block_condition": {
    "type": "origins:command",
    "command": "execute align xyz if entity @e[dy=0,dx=0,dz=0]",
    "comparison": ">=",
    "compare_to": 1
}
```

This example will check if there is an entity inside the block.
