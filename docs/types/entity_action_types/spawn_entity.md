---
title: Spawn Entity (Entity Action Type)
date: 2021-04-05
---

# Spawn Entity

[Entity Action Type](../entity_action_types.md)

Spawns another entity at the position of the target entity.

Type ID: `origins:spawn_entity`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_type` | [Identifier](../data_types/identifier.md) |  | The ID of the entity type that will be spawned.
`tag` | [String](../data_types/string.md) | _optional_ | When set, this NBT data will be applied to the new entity when it is spawned.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | When set, this action will be executed on the new entity when it is spawned.

### Example
```json
"entity_action": {
    "type": "origins:spawn_entity",
    "entity_type": "minecraft:zombie",
    "tag": "{NoAI:1b,IsBaby:1,HandItems:[{id:\"minecraft:gold_block\",Count:1},{}]}"
}
```
This action will spawn a baby zombie holding a gold block at the position, without AI (will not move or act in any way).
