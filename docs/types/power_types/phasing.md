---
title: Phasing (Power Type)
date: 2021-04-08
---

# Phasing

[Power Type](../power_types.md)

Allows the entity that has the power to "phase" (move) through blocks.

Type ID: `apoli:phasing`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`blacklist` | [Boolean](../data_types/boolean.md) | `false` | If set to true, the `block_condition` field will define which blocks the player can **NOT** move through.
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the entity will only be able to move through these blocks (or **not** be able to move through these, depending on what `blacklist` is set to).
`render_type` | [String](../data_types/string.md) | `"blindness"` | Determines how the environment is rendered when "phasing" through (moving) blocks. Accepts `"blindness"`, `"remove_blocks"` or `"none"`.
`view_distance` | [Float](../data_types/float.md) | `10.0` | Determines how far the player can look through walls when "phasing" (moving) through blocks when `render_type` is set to `"blindness"`.
`phase_down_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, the entity will only be able to "phase" (move) downwards if this condition is fulfilled.


### Examples

```json
{
  	"type": "apoli:phasing",
  	"blacklist": true,
  	"render_type": "blindness",
  	"view_distance": 10,
  	"block_condition": {
    	"type": "apoli:in_tag",
    	"tag": "test:phase_blacklist"
  	},
  	"phase_down_condition": {
    	"type": "apoli:and",
    	"conditions": [
      		{
        		"type": "apoli:sneaking"
      		},
      		{
        		"type": "apoli:on_block"
      		}
    	]
  	}
}
```

This example will allow the player to phase through all blocks except for those in the `test:phase_blacklist` (`data/test/tags/blocks/phase_blacklist.json`) block tag. They can also phase down while sneaking, but will make a short stop at each block so they don't take fall damage.
