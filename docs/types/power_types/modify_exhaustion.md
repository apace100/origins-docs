---
title: Modify Exhaustion (Power Type)
date: 2021-04-06
---

# Modify Exhaustion

[Power Type](../power_types.md)

Modifies the amount of exhaustion the player receives each time they receive exhaustion.

Type ID: `apoli:modify_exhaustion`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the received exhaustion amount.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the received exhaustion amount.



### Examples

```json
{
    "type": "apoli:modify_exhaustion",
    "modifier": {
        "name": "Increased exhaustion",
        "operation": "multiply_base",
        "value": 2.0
    }
}
```

This example triples the exhaustion rate of the player.
