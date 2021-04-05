---
title: Origin
date: 2021-04-04
---
# Origin

[Entity Condition](../entity_conditions.md).

Checks whether the player has a certain origin (optionally in a certain layer). Mostly used for [Origin conditions in layers](../misc/origin_conditions_in_layers).

Type ID: `origins:origin`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`origin` | [String](../data_types/string.md) | |  _ID of the origin the player needs to have to pass the check._
`layer` | [String](../data_types/string.md) | _Optional_ |  _If set, will check only the layer with the provided ID for the origin._
