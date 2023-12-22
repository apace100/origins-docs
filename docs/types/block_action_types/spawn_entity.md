---
title: Spawn Entity (Block Action Type)
date: 2023-10-26
---


#	Spawn Entity

[Block Action Type](../block_action_types.md)

Spawns an entity at the position of the block.

Type ID: `origins:spawn_entity`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_type` | [Identifier](../data_types/identifier.md) | | The ID of the type of entity that will be spawned.
`tag` | [NBT](../data_types/nbt.md) | *optional* | If specified, this NBT data will be applied to the entity that will be spawned.
`entity_action` | [Entity Action Type](../entity_action_types.md) | *optional* | If specified, this entity action will be executed on the spawned entity.


###	Examples

```json
"block_action": {
	"type": "origins:spawn_entity",
	"entity_type": "minecraft:vex",
	"entity_action": {
		"type": "origins:grant_power",
		"power": "origins:arcane_skin",
		"source": "*:*"
	}
}
```

This example will summon a Vex with the power `origins:arcane_skin` power with the source as the ID of the example power at the position of the block.
