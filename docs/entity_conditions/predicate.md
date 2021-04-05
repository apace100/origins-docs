---
title: Predicate
date: 2021-04-04
---
# Predicate

[Entity Condition](../entity_conditions.md).

Checks whether the entity fulfills a certain [predicate](https://minecraft.gamepedia.com/Predicate).

**Note**: due to the nature of predicates, this condition is only effective on the server-side. That means client-based powers, such as triggering active powers, climbing, or making entities glow, won't work with this.

Type ID: `origins:predicate`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`predicate` | [String](../data_types/string.md) | |  _ID of the predicate the entity needs to pass._
