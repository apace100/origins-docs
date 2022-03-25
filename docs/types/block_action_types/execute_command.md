---
title: Execute Command (Block Action Type)
date: 2021-04-05
---

# Execute Command

[Block Action Type](../block_action_types.md)

Executes a command at the position of the block.

Type ID: `apoli:execute_command`

### Fields

| Field     | Type                              | Default | Description             |
| --------- | --------------------------------- | ------- | ----------------------- |
| `command` | [String](../data_types/string.md) |         | The command to execute. |

### Examples

```json
"block_action": {
    "type": "apoli:execute_command",
    "command": "summon minecraft:item ~ ~ ~ {Item:{id:\"minecraft:wheat\",Count:1}}"
}
```

This example will summon a Wheat item entity at the position of the block action type.
