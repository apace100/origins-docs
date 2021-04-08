---
title: Phasing (Power Type)
date: 2021-04-08
---
# Phasing

[Power Type](../power_types.md).

Lets the player move through solid blocks.

Type ID: `origins:phasing`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`blacklist` | [Boolean](../data_types/boolean.md) | false | If set to true, the `block_condition` will define which blocks the player can NOT move through.
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | If set, the player will only be able to move through these blocks (or not be able to move through these, depending on what `blacklist` is set to).
`render_type` | [String](../data_types/string.md) | "blindness" | Either "remove_blocks" or "blindness" - defines how the phasing will look when inside a block.
`view_distance` | [Float](../data_types/float.md) | 10.0 | How far the player can look through walls while phasing with the "blindness" `render_type`.
`phase_down_condition` | [Entity Condition](../block_conditions.md) | _optional_ | When specified, this condition needs to be fulfilled in order for blocks below the player to become phasable. Defaults to a condition which checks for sneaking.

### Example
```json
{
  	"type": "origins:phasing",
  	"blacklist": true,
  	"render_type": "blindness",
  	"view_distance": 10,
  	"block_condition": {
    	"type": "origins:in_tag",
    	"tag": "origins:unphasable"
  	},
  	"phase_down_condition": {
    	"type": "origins:and",
    	"conditions": [
      		{
        		"type": "origins:sneaking"
      		},
      		{
        		"type": "origins:on_block"
      		}
    	]
  	}
}
```
This power allows players to phase through all blocks except for those in the unphasable tag. They will also phase down while sneaking, but will make a short stop at each block so they don't take fall damage.
