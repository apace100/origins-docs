---
title: Modifier Operation (Data Type)
date: 2021-04-04
---

# Modifier Operation

[Data Type](../data_types.md)

A [String](string.md) used to specify an operation used by [Attribute Modifiers](attribute_modifier.md) and [Attributed Attribute Modifiers](attributed_attribute_modifier.md).

!!! note

    The listed values are ordered based on the order of priority, with `add_base_early` executing before other modifiers, and `set_total` overriding everything else.

### Values

Value                           | Description
--------------------------------|------
`add_base_early`                | Adds (or subtracts) the modifier value to the base: `NewValue = BaseValue + ModifierValue`
`multiply_base_additive`        | Adds (or subtracts) a portion of the base value: `NewValue = CurrentValue + (BaseValue * ModifierValue)`
`multiply_base_multiplicative`  | Multiplies the base value by this value: `NewValue = CurrentValue + (1 + ModifierValue)`
`add_base_late`                 | Adds (or subtracts) a modifier value to the base: `NewValue = BaseBalue + ModifierValue`
`min_base`                      | Prevents the base value from going below this value: `MinimumBaseValue = ModifierValue`
`max_base`                      | Prevents the base value from going above this value: `MaximumBaseValue = ModifierValue`
`set_base`                      | Sets the base value to the modifier value: `NewValue = ModifierValue`
`multiply_total_additive`       | Multiplies the total value by this value: `NewTotalValue = TotalValue * (1 + ModifierValue)`
`multiply_total_multiplicative` | Multiplies the total value by this value: `NewTotalValue = TotalValue * (1 + ModifierValue)`
`add_total_late`                | Adds (or subtracts) the modifier value to the total: `NewTotalValue = TotalValue + ModifierValue`
`min_total`                     | Prevents the total value from going below this value: `MinimumTotalValue = ModifierValue`
`max_total`                     | Prevents the total value from going above this value: `MaximumTotalValue = ModifierValue`
`set_total`                     | Sets the total value to this value: `NewTotalValue = ModifierValue`

### Legacy Values
These values are redundant as of 1.6.0, but still function and may be removed at a later date.

Value            | Description
-----------------|------
`addition`       | Adds (or subtracts) the modifier value to the base: `NewValue = BaseValue + ModifierValue`
`multiply_base`  | Adds (or subtracts) a portion of the base value: `NewValue = CurrentValue + (BaseValue * ModifierValue)`
`multiply_total` | Multiplies the total value by this value: `NewTotalValue = TotalValue * (1 + ModifierValue)`


### Examples

```json
{
    "operation": "multiply_total"
}
```

Will multiply the total value.
<br>

```json
"modifier": {
    "attribute": "reach-entity-attributes:reach",
    "operation": "addition",
    "value": -2
}
```

A modifier operation used inside an [Attributed Attribute Modifier](attributed_attribute_modifier.md), which subtracts 2 blocks from the player's block reach.
