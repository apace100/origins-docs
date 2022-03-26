---
title: Origin (Predicate)
date: 2021-12-01
---

#   Origin

[Predicate](../predicates.md)

Checks if the player has the specified origin.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`origin` | [Identifier](../../types/data_types/identifier.md) | | The namespace and ID of the origin that you want to check for.


### Examples

```json
{
    "condition": "origins:origin",
    "origin": "origins:human"
}
```

This example will check if the player has the `origins:human` origin.
