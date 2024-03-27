---
title: Enchantment (Entity Condition Type)
date: 2021-04-04
---

# Enchantment

[Entity Condition Type](../entity_condition_types.md)

Checks the level of an enchantment on the entity's equipment.

Type ID: `origins:enchantment`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the enchantment of interest.
`calculation` | [String](../data_types/string.md) | `"sum"` | Which number to compare - either the `sum` of levels of this enchantment on all of the player's equipment, or the `max` level of this enchantment on any of the player's equipment.
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the level of the specified enchantment should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value at which the level of the specified enchantment will be compared to.


### Examples

```json
"condition": {
    "type": "origins:enchantment",
    "enchantment": "minecraft:protection",
    "calculation": "sum",
    "comparison": ">=",
    "compare_to": 16
}
```

This condition will check whether the entity is wearing a full set of Protection IV armor (or better, which might be possible with mods).
