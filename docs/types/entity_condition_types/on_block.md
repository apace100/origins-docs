---
title: On Block (Entity Condition Type)
date: 2021-04-04
---

# On Block

[Entity Condition Type](../entity_condition_types.md)

Checks if a block underneath the entity's feet fulfills the specified [Block Condition Type](../block_condition_types.md).

Type ID: `apoli:on_block`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the condition will evaluate to true if the block underneath the entity's feet fulfills the specified block condition type. Otherwise, only check if the entity is on the ground. 


### Examples

```json
"condition": {
    "type": "apoli:on_block"
}
```

This example will check if the entity is currently on the ground.
<br>

```json
"condition": {
    "type": "apoli:on_block",
    "block_condition": {
        "type": "apoli:block",
        "block": "minecraft:grass_block"
    }
}
```

This example will check if the entity is currently on a Grass Block.
