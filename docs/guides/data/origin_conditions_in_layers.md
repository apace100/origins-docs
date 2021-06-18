---
title: Origin conditions in layers
date: 2021-04-28
---
# Origin conditions in layers

Typically, the `origins` field in a layer JSON file looks something like this:

```json
"origins": [
  "origins:avian",
  "origins:blazeborn",
  "origins:enderian",
  "origins:arachnid"
]
```

But, this new feature (0.4.0 and higher) allows you to add conditional origins. This is done by instead of providing a [string](../../data_types/string.md), providing a json [object](../../data_types/object.md) with an [Entity Condition](../../entity_conditions.md):

```json
"origins": [
  "origins:avian",
  "origins:blazeborn",
  {
    "condition": {
      "type": "origins:daytime"
    },
    "origins": [
      "origins:enderian"
    ]
  },
  {
    "condition": {
      "type": "origins:daytime",
      "inverted": true
    },
    "origins": [
      "origins:arachnid"
    ]
  }
]
```

As you can see from the above example, the "conditioned origin objects" can be used alongside the regular strings of origin IDs in the array. Also, the objects contain an array of origins which will be available only when the condition holds. That means you don't have to repeat a condition for several origins if they would have the same condition.

The main use of this feature is for a data pack which provides several layers, and would like to restrict which origins are possible given the previously selected ones (such as first picking an element, and then a fitting origin in the next layer). Specifically for this, the conditions [Origin](../../entity_conditions/origin.md) and [Power](../../entity_conditions/power.md) exist. Example, assuming you have a layer `elemental_origins:element` where you can choose an element:

```json
"origins": [
  {
    "condition": {
      "type": "origins:origin",
      "origin": "elemental_origins:fire",
      "layer": "elemental_origins:element"
    },
    "origins": [
      "origins:blazeborn",
      "elemental_origins:flame_spirit"
    ]
  },
  {
    "condition": {
      "type": "origins:origin",
      "origin": "elemental_origins:air",
      "layer": "elemental_origins:element"
    },
    "origins": [
      "origins:avian",
      "aerum:aerum"
    ]
  },
  "..."
]
```
