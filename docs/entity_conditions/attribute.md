---
title: Attribute
date: 2021-04-04
---
# Attribute

[Entity Condition](../entity_conditions.md).

Applies a check towards a specific attribute value of the player. For a list of attributes available in vanilla, see [Minecraft Wiki: Attributes](https://minecraft.fandom.com/wiki/Attribute#Attributes).

Type ID: `origins:attribute`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`attribute` | [String](../data_types/string.md) | |  _ID of the attribute of which the value should be checked._
`comparison` | [Comparison](../data_types/comparison.md) | |  _How to compare the attribute's value to the specified value._
`compare_to` | [Float](../data_types/float.md) | | _Which value to compare the attribute's value to._

### Example:

```json
"condition": {
  "type": "origins:attribute",
  "attribute": "minecraft:generic.armor",
  "comparison": ">=",
  "compare_to": 10.0
}```

This condition makes a power only activate when the player is wearing enough armor to reach half of the displayed armor protection value.
