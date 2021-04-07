---
title: Or (Condition)
date: 2021-04-07
---
# Or

[Meta Condition](../meta_conditions.md).

This condition checks whether any (meaning 1 or more) of the provided conditions are fulfilled.

Type ID: `origins:or`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`conditions` | [Array](../data_types/array.md) of [Conditions](../conditions.md) | | Any of these conditions have to be fulfilled in order for this condition to be fulfilled.

### Example

```json
"condition": {
  "type": "origins:or",
  "conditions": [
    {
      "type": "origins:status_effect",
      "effect": "minecraft:poison"
    },
    {    
      "type": "origins:status_effect",
      "effect": "minecraft:wither"
    }
  ]
}
```
This condition added to a power activates the power whenever the player is suffering from poison or wither.
