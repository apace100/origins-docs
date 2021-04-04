---
title: Command
date: 2021-04-04
---
# Command

[Entity Condition](../entity_conditions.md).

Compares the result of a command to a specified value.

Type ID: `origins:command`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`command` | [String](../data_types/string.md) | |  _Command to run._
`comparison` | [Comparison](../data_types/comparison.md) | |  _How to compare the command's result to the specified value._
`compare_to` | [Integer](../data_types/integer.md) | | _Which value to compare the command's result to._
`permission_level` | [Integer](../data_types/integer.md) | `4` | _The permission level to use for the command. 0 is a "survival player", anything higher emulates some form of operator. See [Minecraft Wiki (op-permission-level)](https://minecraft.fandom.com/wiki/Server.properties#op-permission-level) for details._
