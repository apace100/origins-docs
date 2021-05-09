---
title: Projectile (Condition)
date: 2021-04-04
---
# Projectile

[Damage Condition](../damage_conditions.md).

Checks whether the damage source was projectile damage, and optionally the type of projectile it was (if specified).

Type ID: `origins:projectile`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`projectile` | [String](../data_types/string.md) | _optional_ | If set, the check will only pass if the projectile was of an entity type with this ID.

### Example
```json
"damage_condition": {
    "type": "origins:projectile",
    "projectile": "minecraft:spectral_arrow"
}
```
This example checks if the damage source projectile entity is a spectral arrow.