---
title: Random Teleport (Entity Action Type)
date: 2023-11-19
---


#	Random Teleport

[Entity Action Type](../entity_action_types.md)

Teleports the entity to a random location within the specified area.

Type ID: `origins:random_teleport`

!!! note

    The actual width and height of the available teleportation area is double the respective provided value, +1 for the block the player stands on in the very center.


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`area_width` | [Float](../data_types/float.md) | `8.0` | Determines the width of the area.
`area_height` | [Float](../data_types/float.md) | `8.0` | Determines the height of the area.
`heightmap` | [Heightmap Type](../data_types/heightmap_type.md) | *optional* | If specified, the location will be anchored above the highest Y level of the world determined by this heightmap type.
`attempts` | [Integer](../data_types/integer.md) | *optional* | Determines how many attempts the entity should be teleported to a random location. Defaults to `area_width` * 2 + `area_height` * 2.
`landing_block_condition` | [Block Condition Type](../block_action_types.md) | *optional* | If specified, the entity will only be teleported on top of a block that fulfills this block condition. Otherwise, the entity will only be teleported on blocks that blocks movement/have solid collision.
`landing_condition` | [Entity Condition Type](../entity_condition_types.md) | *optional* | If specified, the entity will only be teleported to a location if the entity fulfills this entity condition. Otherwise, the entity will only be teleported to a location that is empty (e.g: no blocks and fluids.)
`landing_offset` | [Vector](../data_types/vector.md) | `{"x": 0, "y": 0, "z": 0}` | Determines the offset of the location of where the entity will be teleported. If the X and Z offsets are specified, the X and Z coordinates of the location will be divided (floored) before applying the offset.
`loaded_chunks_only` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the entity should only be teleported in loaded chunks. **It is recommended to keep this set to `true` for performance reasons.**
`success_action` | [Entity Action Type](../entity_action_types.md) | *optional* | If specified, this entity action will be executed on the entity after it's been successfully teleported to a random location.
`fail_action` | [Entity Action Type](../entity_action_types.md) | *optional* | If specified, this entity action will be executed on the entity upon failing to be teleported on a random location.


###	Examples

```json
"entity_action": {
	"type": "origins:random_teleport",
	"area_width": 8,
	"area_height": 8,
	"success_action": {
		"type": "origins:spawn_particles",
		"particle": "minecraft:poof",
		"count": 8
	},
	"fail_action": {
		"type": "origins:execute_command",
		"command": "title @s actionbar {\"text\": \"Cannot teleport!\", \"color\": \"red\"}"
	}
}
```

This example will teleport the entity to a random location within a 17x17x17 area. If the entity has been successfully teleported to a random location, the entity will emit a poof particle, otherwise, a message will pop-up that indicates the entity cannot be teleported.
<br>

```json
"entity_action": {
	"type": "origins:random_teleport",
	"area_width": 4,
	"area_height": 8,
	"landing_block_condition": {
		"type": "origins:in_tag",
		"tag": "minecraft:wool"
	},
	"landing_offset": {
		"x": 0.5,
		"z": 0.5
	}
}
```

This example will teleport the entity on top of the center of a random block included in the `minecraft:wools` block tag within a 9x17x9 area.
