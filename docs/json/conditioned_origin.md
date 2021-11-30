---
title: Conditioned Origin JSON
date: 2021-04-05
---

# Conditioned Origin JSON

An [Object](../types/data_types/object.md) used to specify origins in a [Layer JSON](origin_layer.md) which only show up conditionally.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Entity Condition Type](../types/entity_condition_types.md) | | The entity condition that the player needs to fulfill to get access to the origins specified here.
`origins` | [Array](../types/data_types/array.md) of [Identifiers](../types/data_types/identifier.md) | | Then namespace and IDs of the origins which should become available when the `condition` is fulfilled.


### Examples

```json
{
    "origins": [
        {
            "condition": {
                "type": "origins:daytime",
                "inverted": true
            },
            "origins": [
                "origins:phantom"
            ]
        }
    ]
}
```

This example will make it so that players can only pick the `origins:phantom` origin if it's night time.
