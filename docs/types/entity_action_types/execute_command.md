---
title: Execute Command (Entity Action Type)
date: 2021-04-05
---

# Execute Command

[Entity Action Type](../entity_action_types.md)

Executes a command with the entity as the source (i.e. `@s` will select the entity itself).

Type ID: `apoli:execute_command`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`command` | [String](../data_types/string.md) |  | The command to execute on the entity.


### Examples

```json
"entity_action": {
    "type": "apoli:execute_command",
    "command": "tellraw @a {\"text\": \"Hello world!\", \"color\": \"green\"}"
}
```

This example will execute a `/tellraw` command that will print a green-colored "Hello world!" message to all players.
