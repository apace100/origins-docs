---
title: Attribute Modifier Operation (Data Type)
date: 2021-04-04
---

# Modifier Operation

[Data Type](../data_types.md)

A [string](string.md) used to specify the operation used by [Attribute Modifiers](attribute_modifier.md).

!!! note

    The listed values are ordered based on the order of priority; with `add_base_early` being applied before the other modifiers and `set_total` being applied last.


### Values

Value                           | Description
--------------------------------|---------------
`add_base_early`                | Adds (or subtracts) the modifier value to the base value. (`NewBaseValue = BaseValue + ModifierValue`)
`multiply_base_additive`        | Adds (or subtracts) the base value multiplied by the modifier value to the current base value. (`NewBaseValue = BaseValue + (BaseValue * ModifierValue)`)
`multiply_base_multiplicative`  | Multiplies the current base value by the modifier value. (`NewBaseValue = BaseValue + (1 + ModifierValue)`)
`add_base_late`                 | Adds (or subtracts) the modifier value to the base value. (`NewBaseValue = BaseValue + ModifierValue`)
`min_base`                      | Uses the modifier value as the minimum value for the base value using Java's built-in [`Math#max`](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html#max-double-double-) method. (`NewBaseValue = Math.max(BaseValue, ModifierValue)`)
`max_base`                      | Uses the modifier value as the maximum value for the base value using Java's built-in [`Math#min`](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html#min-double-double-) method. (`NewBaseValue = Math.min(BaseValue, ModifierValue)`)
`set_base`                      | Sets the modifier value as the base value. (`NewBaseValue = ModifierValue`)
`multiply_total_additive`       | Multiplies the total value by the current total value multiplied by the modifier value. (`NewTotalValue = TotalValue * (TotalValue * ModifierValue)`)
`multiply_total_multiplicative` | Multiplies the total value by the modifier value + 1. (`NewTotalValue = TotalValue * (1 + ModifierValue)`)
`min_total`                     | Uses the modifier value as the minimum value for the total value using Java's built-in [`Math#max`](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html#max-double-double-) method. (`NewTotalValue = Math.max(TotalValue, ModifierValue)`)
`max_total`                     | Uses the modifier value as the maximum value for the total value using Java's built-in [`Math#min`](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html#min-double-double-) method. (`NewTotalValue = Math.min(TotalValue, ModifierValue)`)
`set_total`                     | Sets the modifier value as the total value. (`NewTotalValue = ModifierValue`)
