---
title: Riding Recursive (Entity Condition)
date: 2021-10-07
---
# Riding Recursive

[Entity Condition](../entity_conditions.md)

Checks for all the entities that is currently being ridden.

Type ID: `origins:riding_recursive`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, it will only check for the entity/entities that fulfills the bi-entity condition.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the amount of entities currently being ridden should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | Which value the amount of entities currently being ridden should be compared to.