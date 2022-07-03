---
title: Attributed Attribute Modifier Operation (Data Type)
date: 2022-07-03
---

#   Attributed Attribute Modifier Operation

[Data Type](../data_types.md)

A [string](string.md) used to specify the operation used by [Attributed Attribute Modifiers](attributed_attribute_modifier.md).

!!! note

    The listed values are ordered based on the order of priority; with `addition` being applied before `multiply_base` and `multiply_total` being applied last.


### Values

Value            | Description
-----------------|---------------
`addition`       | Adds (or subtracts) the modifier value to the base value. (`NewValue = BaseValue + ModifierValue`)
`multiply_base`  | Adds (or subtracts) the base value multiplied by the modifier value to the base value. (`NewValue = BaseValue + (BaseValue * ModifierValue)`)
`multiply_total` | Multiplies the total value by the modifier value + 1. (`NewTotalValue = TotalValue * (1 + ModifierValue)`)
