---
title: Origin (Predicate)
date: 2021-12-01
---

# Origin

[Predicate](../predicates.md)

Checks if the player has the specified origin.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`origin` | [Identifier](../../types/data_types/identifier.md) | | The namespace and ID of the origin that you want to check for.
`layer` | [Identifier](../../types/data_types/identifier.md) | _optional_ | If specified, only evaluate the predicate to true if the origin is from the specified origin layer.


### Examples

```json
{
    "condition": "origins:origin",
    "origin": "origins:human"
}
```

This example will check if the player has the `origins:human` origin.
<br>

```json
{
    "condition": "origins:origin",
    "origin": "origins:phantom",
    "layer": "origins:origin"
}
```

This example will check if the player has the `origins:phantom` origin in the `origins:origin` origin layer.
