---
title: Brightness
date: 2021-07-04
---
# Brightness

[Entity Condition](../entity_conditions.md).

Checks the brightness at the player's eyes, which ranges from 0 to 1.

Type ID: `origins:brightness`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How to compare the brightness against the specified value.
`compare_to` | [Float](../data_types/float.md) | | Which value to compare the brightness against.

### Brightness calculation

To calculate brightness at the player's eyes, the game first gathers the light level of the block the eyes are inside of. This light level is the highest between the block and sky light levels of the block. Then it calculates brightness with the following formula: `brightness = ambientLight + (1 - ambientLight) * lightLevel / (60 - 3 * lightLevel)`, with `ambientLight` as the dimension's ambient light, which is 0 in the overworld and the End, and 0.1 in the Nether. Thus the formula simplifies to `brightness = lightLevel / (60 - 3 * lightLevel)` for the overworld and the End. The calculated values, however, are slightly off due to [the imprecision of floating point calculations](https://0.30000000000000004.com/).

Here's a table of light levels to brightness levels:

Light level | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15
------------|---|---|---|---|---|---|---|---|---|---|----|----|----|----|----|----
Overworld brightness | 0.0 | 0.017543862 | 0.03703704 | 0.05882353 | 0.08333334 | 0.11111111 | 0.14285715 | 0.17948718 | 0.22222225 | 0.2727273 | 0.33333334 | 0.40740743 | 0.50000006 | 0.6190476 | 0.77777773 | 1.0
Nether brightness | 0.1 | 0.11578947 | 0.13333334 | 0.15294118 | 0.17500001 | 0.2 | 0.22857144 | 0.26153848 | 0.3 | 0.34545457 | 0.4 | 0.4666667 | 0.5500001 | 0.6571428 | 0.79999995 | 1.0

### Example:

```json
"condition": {
    "type": "origins:brightness",
    "comparison": "<=",
    "compare_to": 0.5
}
```
This example will return true if the brightness at the player's eyes is 0.5 or lower, which corresponds to a light level of 11 or below in any of the three default dimensions.
