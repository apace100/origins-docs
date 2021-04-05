---
title: Execute Command (Action)
date: 2021-04-05
---
# Execute Command

[Entity Action](../entity_actions.md).

Executes a command with the entity as the source (i.e. @s will select the entity itself).

Type ID: `origins:execute_command`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`command` | [String](../data_types/string.md) |  | The command to execute (from the perspective of the entity!).
`permission_level` | [Integer](../data_types/integer.md) | `4` | The permission level to use for the command. 0 is a "survival player", anything higher emulates some form of operator. See [Minecraft Wiki (op-permission-level)](https://minecraft.fandom.com/wiki/Server.properties#op-permission-level) for details.

### Example
```json
"entity_action": {
  "type": "origins:execute_command",
  "command": "give @s minecraft:dirt 64",
  "permission_level": 4
}
```
This action gives the entity a stack of dirt.
