---
title: Predicate (Entity Condition Type)
date: 2021-04-04
---

# Predicate

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity fulfills a specified [Predicate](https://minecraft.wiki/w/Predicate).

Type ID: `origins:predicate`

!!! caution

    This entity condition type only operates on the <span style="color:goldenrod"><b>server-side</b></span>, meaning that it cannot be used in fields that are evaluated on the client-side.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`predicate` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the predicate the entity needs to pass.


### Examples

```json
"condition": {
    "type": "origins:predicate",
    "predicate": "example:weather/is_thunderstorm"
}
```

This example will check if the `example:check_if_thunderstorm` predicate (`data\example\predicates\weather\is_thunderstorm.json`) is true.
<br>

```json
{
    "condition": "minecraft:weather_check",
    "raining": true,
    "thundering": true
}
```

This being the contents of the `example:check_if_thunderstorm` predicate. (`data\example\predicates\weather\is_thunderstorm.json`)
