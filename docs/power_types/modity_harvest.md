---
title: Modify Harvest (Power Type)
date: 2021-04-06
---
# Modify Harvest

[Power Type](../power_types.md).

Modifies whether a player is able to harvest a block or not (= receive the block drops).

Type ID: `origins:modify_harvest`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions) | _optional_ | If set, the modification will only apply to blocks which satisfy this condition.
`allow` | [Boolean](../data_types/boolean.md) | _optional_ | When true, the player will be able to harvest the blocks. When false, the player will not be able to harvest the blocks.
