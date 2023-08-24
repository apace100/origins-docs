---
title: Command (Entity Condition Type)
date: 2021-04-04
---

# Command

[Entity Condition Type](../entity_condition_types.md)

Compares the result of the specified command to the specified value.

Type ID: `origins:command`

!!! caution

    This entity condition type only operates on the <span style="color:goldenrod"><b>server-side</b></span>, meaning that it cannot be used in fields that are evaluated on the client-side.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`command` | [String](../data_types/string.md) | |  The command to execute.
`comparison` | [Comparison](../data_types/comparison.md) | | How to compare the stored result of the specified command to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value to compare the stored result of the specified command to.


### Examples

```json
"condition": {
    "type": "origins:command",
    "command": "execute if score @s objective1 = @s objective2",
    "comparison": "==",
    "compare_to": 1
}
```
This example will check if the entity has the same score in the `objective1` and `objective2` scoreboard objectives.
<br>

```json
"condition": {
    "type": "origins:command",
    "command": "execute if entity @e[type = #minecraft:skeletons, distance = ..64]",
    "comparison": ">=",
    "compare_to": 4
}
```

This example will check if there are 4 or more entities that are included in the `#minecraft:skeletons` (`data/minecraft/tags/entity_types/skeletons.json`) entity type tag within a 64 blocks spherical radius relative to the entity.
