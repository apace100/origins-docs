---
title: Conditioned Origin JSON
date: 2021-04-05
---

# Conditioned Origin JSON

An [Object](data_types/object.md) used to specify origins in a [Layer JSON](layer_json.md) which only show up conditionally.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Entity Condition](entity_conditions.md) | | The condition that the player needs to fulfill to get access to the origins specified here.
`origins` | [Array](data_types/array.md) of [Identifiers](data_types/identifier.md) | | IDs of the origins which should become available when the `condition` is fulfilled.

### Example

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
This example makes it so that players can only pick the `origins:phantom` origin if it's night time.