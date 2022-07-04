---
title: Result Type (Data Type)
date: 2022-07-03
---

#   Result Type

[Data Type](../data_types.md)

A [string](string.md) that is used to determine which item stack to use as a new result item stack.

!!! note

    This data type is only used by the [Modify Grindstone (Power Type)](../power_types/modify_grindstone.md)


### Values

Value         | Description
--------------|------------
`unchanged`   | The initial item stack will not be changed.
`specified`   | The initial item stack will be replaced by the specified item stack.
`from_top`    | The initial item stack will be replaced by the item stack from the top input slot of a Grindstone.
`from_bottom` | The initial item stack will be replaced by the item stack from the bottom input slot of a Grindstone.
