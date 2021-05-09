---
title: Power Active
date: 2021-04-04
---
# Power Active

[Entity Condition](../entity_conditions.md).

Checks whether another power is active (meaning the player has the power and the power has all conditions fulfilled).

Type ID: `origins:power_active`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | |  ID of the power which will be checked for being active.

### Example:
```json
"condition": {
    "type": "origins:power_active",
    "power": "origins:phantomize"
}
```
This example checks if the [`origins:phantomize`](https://github.com/apace100/origins-fabric/blob/master/src/main/resources/data/origins/powers/phantomize.json) power is toggled on.