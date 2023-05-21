---
title: Projectile (Damage Condition Type)
date: 2021-04-04
---

# Projectile

[Damage Condition Type](../damage_condition_types.md)

Checks whether the damage source was projectile damage, and optionally the type of projectile it was (if specified).

Type ID: `origins:projectile`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`projectile` | [Identifier](../data_types/identifier.md) | _optional_ | If set, the check will only pass if the projectile was of an entity type with the specified namespace and ID.
`projectile_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If set, the check will only pass if the projectile entity fulfills this condition.

### Examples

```json
"damage_condition": {
    "type": "origins:projectile",
    "projectile": "minecraft:spectral_arrow"
}
```

This example will check if the damage source is a Spectral Arrow projectile entity.
<br>

```json
"damage_condition": {
    "type": "origins:projectile",
    "projectile_condition": {
      "type": "origins:and",
      "conditions": [
        {
          "type": "origins:entity_type",
          "entity_type": "minecraft:arrow"
        },
        {
          "type": "origins:on_fire"
        }
      ]
    }
}
```

This example will check if the damage source is a burning arrow.
