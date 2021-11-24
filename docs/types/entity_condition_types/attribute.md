---
title: Attribute (Entity Condition Type)
date: 2021-04-04
---

# Attribute

[Entity Condition Type](../entity_condition_types.md)

Applies a check towards a specific attribute value of the entity.

Type ID: `origins:attribute`

!!! note

    For a list of attributes available in vanilla, see [Minecraft Fandom Wiki: Attributes](https://minecraft.fandom.com/wiki/Attribute#Attributes).

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`attribute` | [Identifier](../data_types/identifier.md) | |  ID of the attribute of which the value should be checked.
`comparison` | [Comparison](../data_types/comparison.md) | |  How to compare the attribute's value to the specified value.
`compare_to` | [Float](../data_types/float.md) | | Which value to compare the attribute's value to.

### Example:

```json
"condition": {
    "type": "origins:attribute",
    "attribute": "minecraft:generic.armor",
    "comparison": ">=",
    "compare_to": 10.0
}
```

This condition makes a power only activate when the player is wearing enough armor to reach half of the displayed armor protection value.
