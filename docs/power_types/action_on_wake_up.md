---
title: Action On Wake Up (Power Type)
date: 2021-04-04
---
# Action On Wake Up

[Power Type](../power_types.md).

Executes an entity action or a block action when the player wakes up after sleeping.

Type ID: `origins:action_on_wake_up`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player when they wake up.
`block_action` | [Block Action](../block_actions.md) | _optional_ | If set, this action will be executed on the bed block.
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | If set, the actions will only trigger when this block condition is met by the bed block.
