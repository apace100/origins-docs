---
title: Name (Condition)
date: 2021-04-04
---
# Name

[Damage Condition](../damage_conditions.md).

Checks whether the damage source has a specific name (essentially checking the type of damage).

Type ID: `origins:name`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`name` | [String](../data_types/string.md) | |  Name the damage source should have to pass the check. See [List of vanilla damage source names](../misc/vanilla_damage_sources.md).

### Example
```json
"damage_condition": {
    "type": "origins:name",
    "name": "inWall"
}
```
This example checks if the damage source is `inWall`, which means that the player is suffocating in a block.