---
title: Food Component (Data Type)
date: 2023-10-09
---

# Food Component

[Data Type](../data_types.md)

An [object](object.md) which defines a new food component.

!!! note

    The actual food saturation level is determined by the `food * saturation * 2` formula.


### Fields

Field                                                       |   Type                                                                                            |   Default                                             |   Description
------------------------------------------------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|--------------
`nutrition`                                                 |   [Integer](../data_types/integer.md)                                                             |                                                       |   Determines the amount of hunger shanks (half a shank = 1) the food component recovers from consumption.
`saturation`                                                |   [Float](../data_types/float.md)                                                                 |                                                       |   Determines the amount of saturation to give to the player upon consumption.
[`can_always_eat`](## "Previous names: ["always_edible"]")  |   [Boolean](../data_types/boolean.md)                                                             |   `false`                                             |   Determines whether the food component can always be eaten anytime.
`eat_seconds`                                               |   [Float](../data_types/float.md)                                                                 |   `1.6`                                               |   Determines the seconds of which the food will be consumed for.
`meat`                                                      |   [Boolean](../data_types/boolean.md)                                                             |   <span style="color:darkred"><b>REMOVED</b></span>   |   Food components no longer have the meat property. **Include the item in either the `#minecraft:meat` or `#minecraft:wolf_food` item tag instead**.
`snack`                                                     |   [Boolean](../data_types/boolean.md)                                                             |   <span style="color:darkred"><b>REMOVED</b></span>   |   **Use `eat_seconds` instead.** (Using a value of `0.8` is equivalent to this field being true.)
`using_converts_to`                                         |   [Item Stack](../data_types/item_stack.md)                                                       |   _optional_                                          |   If specified, the consumed item stack will be converted into this item stack.
`effect`                                                    |   [Food Effect Entry](../data_types/food_effect_entry.md)                                         |   _optional_                                          |   If specified, this effect (with the specified chance) will be applied upon consumption.
`effects`                                                   |   [Array](../data_types/array.md) of [Food Effect Entries](../data_types/food_effect_entry.md)    |   _optional_                                          |   If specified, these effects (with the specified chances) will be applied upon consumption.



### Examples

```json
"food_component": {
    "nutrition": 4,
    "saturation": 1.0
}
```

A food component that recovers 2 hunger shanks and 8 saturation points.
