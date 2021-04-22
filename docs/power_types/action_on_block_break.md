---
title: Action On Block Break (Power Type)
date: 2021-04-04
---
# Action On Block Break

[Power Type](../power_types.md).

Executes an entity action or a block action when the player breaks a block.

Type ID: `origins:action_on_block_break`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player when a block is broken.
`block_action` | [Block Action](../block_actions.md) | _optional_ | If set, this action will be executed on the block that is broken.
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | If set, the actions will only trigger when this block condition is met by the broken block.
`only_when_harvested` | [Boolean](../data_types/boolean.md) | true | If this is true, the actions will only execute when the player succeeds in harvesting the block (e.g. they will not trigger when stone is broken by hand).


### Example
```json
{
    "type": "origins:action_on_block_break",
    "entity_action": {
        "type": "origins:damage",
        "amount": 2.0,
        "source": {
            "name": "onFire",
            "bypasses_armor": true,
            "fire": true
        }
    },
    "block_action": {
        "type": "origins:set_block",
        "block": "minecraft:lava"
    },
    "block_condition": {
        "type": "origins:block",
        "block": "minecraft:magma_block"
    },
    "only_when_harvested": false
}
```
If a player with this power has mined a magma block, it'll deal 1 heart of \[`onFire`\] damage to the player, and place a lava block at where the magma block previously was.