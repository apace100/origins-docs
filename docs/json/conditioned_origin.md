---
title: Conditioned Origin JSON
date: 2021-04-05
---

# Conditioned Origin JSON

An [Object](../types/data_types/object.md) used to specify origins in a [Layer JSON](origin_layer.md) which only show up conditionally.

!!! note

    Check [Origin conditions in layers](../guides/data/origin_conditions_in_layers.md) for a detailed guide on how to use this feature.

!!! caution

    The entity condition specified in the `condition` field is only evaluated on the <span style="color:goldenrod"><b>client-side</b></span>, therefore, using entity condition types that only work on the server-side will not work.




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
