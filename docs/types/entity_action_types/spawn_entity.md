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
`entity_type` | [Identifier](../data_types/identifier.md) |  | The namespace and ID of the entity type that will be spawned.
`tag` | [NBT](../data_types/nbt.md) | _optional_ | If specified, this NBT data will be applied to the entity that will be spawned.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, the specified entity action type will be executed on the entity that will be spawned when it is spawned.
`bientity_action` | [Bi-Entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this bi-entity action will be executed on either or both the actor (the entity that invoked the entity action) and the target (the spawned entity).


### Examples

```json
"entity_action": {
    "type": "origins:spawn_entity",
    "entity_type": "minecraft:zombie",
    "tag": "{NoAI:1b,IsBaby:1,HandItems:[{id:\"minecraft:gold_block\",Count:1},{}]}"
}
```

This example will spawn a baby Zombie holding a Gold Block that has no AI at the position of the entity.
