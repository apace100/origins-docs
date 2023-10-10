---
title: Food Component (Data Type)
date: 2023-10-09
---

# Food Component

[Data Type](../data_types.md)

An [Object](object.md) which defines a new food component.


### Fields

Field  | Type | Default | Description
-------|-----|---------------|-------------
`hunger` | [Integer](../data_types/integer.md) | | The amount of hunger shanks the food component recovers upon consumption.
`saturation` | [Float](../data_types/float.md) | | The amount of saturation to give the player upon consumption.
`meat` | [Boolean](../data_types/boolean.md) | `false` | Whether this food component counts as meat or not.
`always_edible` | [Boolean](../data_types/boolean.md) | `false` | Whether this food component is edible at full hunger or not.
`snack` | [Boolean](../data_types/boolean.md) | `false` | Whether this food component takes as long as dried kelp to eat (16 ticks) or not (32 ticks).
`effect` | [Status Effect Instance](../data_types/status_effect_instance.md) | _optional_ | A status effect and the chance of it triggering upon consuming something with this food component.
`effects` | [Array](../data_types/array.md) of [Status Effect Instances](../data_types/status_effect_instance.md) | _optional_ | A status effect and the chance of it triggering upon consuming something with this food component.


### Examples

```json
"food_component": {
    "hunger": 4,
    "saturation": 1.0
}
```

A food component that recovers 4 hunger and 1 saturation.
