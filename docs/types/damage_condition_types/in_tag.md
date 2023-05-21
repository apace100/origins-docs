---
title: In Tag (Damage Condition Type)
date: 2023-05-21
---

# In Tag

[Damage Condition Type](../damage_condition_types.md)

Checks whether the type of this damage is in a specified tag.

Type ID: `origins:in_tag`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`tag` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the tag which the damage type should be in to pass the check.


### Examples

```json
"condition": {
    "type": "origins:in_tag",
    "tag": "minecraft:is_drowning"
}
```

This example will check if the damage is considered drowning damage.
