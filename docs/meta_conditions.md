---
title: Meta Conditions
date: 2021-04-07
---
# Meta Conditions

Meta Conditions are independent of the type they operate on. They basically combine or modify other conditions. The conditions which are modified have to be of the type the field of the meta condition requires. For example, if you have a field which requires an [Entity Condition](entity_conditions.md) and you insert an [And](and) meta condition, the conditions you need to provide inside that conditions will have to be [Entity Conditions](entity_conditions.md) as well.

## List

* [And](meta_conditions/and.md)
* [Constant](meta_conditions/constant.md)
* [Not](meta_conditions/not.md)
* [Or](meta_conditions/or.md)

## Block Conditions

* [Offset](meta_conditions/offset.md)

### Bi-entity Conditions

* [Actor Condition](meta_conditions/actor_condition.md)
* [Both](meta_conditions/both.md)
* [Either](meta_conditions/either.md)
* [Invert](meta_conditions/invert.md)
* [Target Condition](meta_conditions/target_condition.md)
* [Undirected](meta_conditions/undirected.md)
