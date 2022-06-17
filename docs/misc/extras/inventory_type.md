---
title: Inventory Type (Extras)
date: 2022-06-15
---

#   Inventory Type

[Extra](../extras.md)

A [string](../../types/data_types/string.md) used to determine whether to reference the inventory of the entity or the inventory of a power present in the entity.

!!! note

    Not to be confused with [Container Type](container_type.md)


### Values

Value | Description
------|------------
`inventory` | Determines that the inventory of the entity will be referenced, assuming they can have one.
`power` | Determines that the inventory of a power that uses the [Inventory (Power Type)](../../types/power_types/inventory.md) will be referenced.
