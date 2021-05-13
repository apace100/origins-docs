---
title: Modify Exhaustion (Power Type)
date: 2021-04-06
---
# Modify Exhaustion

[Power Type](../power_types.md).

Modifies the amount of exhaustion the player receives each time they receive exhaustion.

Type ID: `origins:modify_exhaustion`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If set, this modifier will apply to the exhaustion amount.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, these modifiers will apply to the exhaustion amount.


### Example
```json
{
    "type": "origins:modify_exhaustion",
    "modifier": {
        "name": "Increased exhaustion",
        "operation": "multiply_base",
        "value": 2.0
    }
}
```
This power triples the exhaustion rate of the player.
