---
title: Execute Command (Entity Action)
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

### Example
```json
"entity_action": {
  "type": "origins:execute_command",
  "command": "give @s minecraft:dirt 64"
}
```
This action gives the entity a stack of dirt.
