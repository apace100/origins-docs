---
title: Attribute Modifier Operation (Data Type)
date: 2021-04-04
---

# Modifier Operation

[Data Type](../data_types.md)

A [String](string.md) used to specify the operation used by [Attribute Modifiers](attribute_modifier.md).

!!! note

    The listed values are ordered based on the order of priority; with `add_base_early` being applied before the other modifiers and `set_total` being applied last.


### Values

Value                           | Description
--------------------------------|---------------
`add_base_early`                | Adds the modifier value to the base value. (`NewBaseValue = BaseValue + ModifierValue`)
`multiply_base_additive`        | Adds the base value multiplied by the modifier value to the current base value. (`NewBaseValue = BaseValue + (BaseValue * ModifierValue)`)
`multiply_base_multiplicative`  | Multiplies the current base value by the modifier value. (`NewBaseValue = BaseValue * (1 + ModifierValue)`)
`add_base_late`                 | Adds the modifier value to the base value. (`NewBaseValue = BaseValue + ModifierValue`)
`min_base`                      | Sets the bigger value between the base value and the modifier value as the new base value. (`NewBaseValue = (BaseValue > ModifierValue ? BaseValue : ModifierValue)`)
`max_base`                      | Sets the smaller value between the base value and the modifier value as the new base value. (`NewBaseValue = (BaseValue < ModifierValue ? BaseValue : ModifierValue)`)
`set_base`                      | Sets the modifier value as the new base value. (`NewBaseValue = ModifierValue`)
`multiply_total_additive`       | Multiplies the total value by the current total value multiplied by the modifier value. (`NewTotalValue = TotalValue * (TotalValue * ModifierValue)`)
`multiply_total_multiplicative` | Multiplies the total value by the modifier value + 1. (`NewTotalValue = TotalValue * (1 + ModifierValue)`)
`min_total`                     | Sets the bigger value between the total value and the modifier value as the new total value. (`NewTotalValue = (TotalValue > ModifierValue ? TotalValue : ModifierValue)`)
`max_total`                     | Sets the smaller value between the total value and the modifier value as the new total value. (`NewTotalValue = (TotalValue < ModifierValue ? TotalValue : ModifierValue)`)
`set_total`                     | Sets the modifier value as the new total value. (`NewTotalValue = ModifierValue`)
