---
title: Name (Damage Condition Type)
date: 2021-04-04
---

# Name

[Damage Condition Type](../damage_condition_types.md)

Checks whether the damage source has a specific name (essentially checking the type of damage).

Type ID: `origins:name`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`name` | [String](../data_types/string.md) | |  Name the damage source should have to pass the check. See [List of Damage Source Names](../../misc/extras/damage_source_names.md) for possible values.


### Examples

```json
"damage_condition": {
    "type": "origins:name",
    "name": "inWall"
}
```

This example will check if the damage source name is `inWall`, meaning that the condition will evaluate to true if the entity is suffocating in a block.
