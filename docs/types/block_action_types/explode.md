---
title: Explode (Block Action Type)
date: 2021-11-30
---

# Explode

[Block Action Type](../block_action_types.md)

Summons an explosion with a specific explosion power.

Type ID: `origins:explode`

!!! note

    See [Minecraft Wiki: Explosion (Causes)](https://minecraft.wiki/w/Explosion#Causes) for a list of power values that are used in vanilla.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Float](../data_types/float.md) | | Determines the power of the explosion.
`destruction_type` | [Destruction Type](../data_types/destruction_type.md) | `"break"` | Determines the effect of the explosion to the terrain.
`indestructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the blocks that fulfill this condition will not be destroyed by the summoned explosion.
`destructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, only the blocks that fulfill this condition will be destroyed by the summoned explosion.
`create_fire` | [Boolean](../data_types/boolean.md) | `false` | Determines if the summoned explosion should create fire.


### Examples

```json
"block_action": {
    "type": "origins:explode",
    "power": 5,
    "destruction_type": "none",
    "create_fire": false
}
```

This example will summon an explosion at the position of where the block action was invoked that would not destroy the terrain nor spread fire.
<br>


```json
"block_action": {
    "type": "origins:explode",
    "power": 5,
    "destruction_type": "break",
    "destructible": {
        "type": "apoli:in_tag",
        "tag": "minecraft:impermeable"
    },
    "create_fire": false
}
```

This example will summon an explosion at the position of where the block action was invoked that would only destroy blocks that are in the `#minecraft:impermeable` (`data/minecraft/tags/blocks/impermeable.json`) block tag.
