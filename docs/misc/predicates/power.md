---
title: Power (Predicate)
date: 2022-06-15
---

# Power

[Predicate](../predicates.md)

Checks if the entity has the specified power.

Type ID: `apoli:power`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | [Identifier](../../types/data_types/identifier.md) | | The namespace and ID of the power to check for.
`source` | [Identifier](../../types/data_types/identifier.md) | _optional_ | If specified, checks if the specified power is from this power source.


### Examples

```json
{
    "condition": "apoli:power",
    "power": "origins:arcane_skin"
}
```

This example will check if the player has the `origins:arcane_skin` power.
<br>

```json
{
    "condition": "apoli:power",
    "power": "origins:water_breathing",
    "source": "origins:merling"
}
```

This example will check if the player has the `origins:water_breathing` power from the `origins:merling` power source.
