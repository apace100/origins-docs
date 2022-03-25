---
title: Projectile (Damage Condition Type)
date: 2021-04-04
---

# Projectile

[Damage Condition Type](../damage_condition_types.md)

Checks whether the damage source was projectile damage, and optionally the type of projectile it was (if specified).

Type ID: `apoli:projectile`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`projectile` | [Identifier](../data_types/identifier.md) | _optional_ | If set, the check will only pass if the projectile was of an entity type with the specified namespace and ID.


### Examples

```json
"damage_condition": {
    "type": "apoli:projectile",
    "projectile": "minecraft:spectral_arrow"
}
```

This example will check if the damage source is a Spectral Arrow projectile entity.
