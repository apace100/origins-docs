---
title: Attacker (Condition)
date: 2021-04-04
---
# Attacker

[Damage Condition](../damage_conditions.md).

Checks whether the condition has an attacker, and optionally whether the attacker fulfills a specified [Entity Condition](../entity_conditions.md).

Type ID: `origins:attacker`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition](../entity_conditions.md) | |  _optional: If set, the attacking entity must fulfill the provided entity condition in order for this condition to evaluate to true._
