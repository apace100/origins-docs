---
title: Execute Command (Block Action)
date: 2021-04-05
---
# Execute Command

[Block Action](../block_actions.md).

Executes a command at the position of the block.

Type ID: `origins:execute_command`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`command` | [String](../data_types/string.md) |  | The command to execute.

### Example
```json
"block_action": {
  "type": "origins:execute_command",
  "command": "summon minecraft:item ~ ~ ~ {Item:{id:\"minecraft:wheat\",Count:1}}"
}
```
Creates a wheat item at the position of the block the action is executed on.
