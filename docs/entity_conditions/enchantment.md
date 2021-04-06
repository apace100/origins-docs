---
title: Enchantment (Condition)
date: 2021-04-04
---
# Enchantment

[Entity Condition](../entity_conditions.md).

Checks the level of an enchantment on the entity's equipment.

Type ID: `origins:enchantment`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [Identifier](../data_types/identifier.md) | | ID of the enchantment of interest.
`calculation` | [String](../data_types/string.md) | "sum" | Which number to compare - either the `sum` of levels of this enchantment on all of the player's equipment, or the `max` level of this enchantment on any of the player's equipment.
`comparison` | [Comparison](../data_types/comparison.md) | | How the enchantment level should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value to compare the enchantment level to.

### Example:

```json
"condition": {
  "type": "origins:enchantment",
  "enchantment": "minecraft:protection",
  "calculation": "sum",
  "comparison": ">=",
  "compare_to": 16
}
```
This condition checks whether the entity is wearing a full set of Protection IV armor (or better, which might be possible with mods).
