---
title: Scoreboard (Entity Condition Type)
date: 2021-04-04
---

# Scoreboard

[Entity Condition Type](../entity_condition_types.md)

Compares the score of the entity from a specified scoreboard objective to a specified value.

Type ID: `origins:scoreboard`


!!! note

    If the player does not have the scoreboard objective, this condition would always return false (even if `"!="` is used). You can then use the `"!="` comparison in combination with the `"=="` comparison to test if the player does not have this objective set (for example, if a player has newly joined a world or had their objectives reset).


!!! caution

    This entity condition type only operates on the <span style="color:goldenrod"><b>server-side</b></span>, meaning that it cannot be used in fields that are evaluated on the client-side.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`name` | [String](../data_types/string.md) | _optional_ | If specified, the condition will check for the score of this score holder.
`objective` | [String](../data_types/string.md) | | The name of the scoreboard objective to retrieve the value from and compare.
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the score of the specified score holder should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value at which the score of the specified score holder will be compared to.


### Examples

```json
"condition": {
    "type": "origins:scoreboard",
    "objective": "obj",
    "comparison": ">",
    "compare_to": 3
}
```

This example will check if the score of the player in the `obj` scoreboard objective is greater than 3.
