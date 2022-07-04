---
title: Replace Loot Table (Power Type)
date: 2022-07-03
---

#   Replace Loot Table

[Power Type](../power_types.md)

Replaces a loot table with another loot table.

Type ID: `origins:replace_loot_table`

!!! note

    The keys in the `replace` object field are formatted as a regular expression, where matching loot table namespace, path and IDs will be replaced with the specified value. See [Wikipedia: Regular expression](https://en.wikipedia.org/wiki/Regular_expression) for more information about regular expressions and [RegExr](https://regexr.com/) to test regular expressions online.

!!! note

    In the context of this power type, the '**actor**' entity is the entity that has the power while the '**target**' entity depends on the context of the loot tables that'll be replaced.

    Here's a table for possible instances the '**target**' entity could be:

    Loot Type  | Target Entity
    -----------|-------
    Barter     | The Piglin that was bartered with.
    Block      | The '**actor**' entity that mined the block.
    Chest      | The '**actor**' entity that opened the Chest.
    Entity     | The entity that died.
    Fishing    | The '**actor**' entity's fishing bobber.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`replace` | [Object](../data_types/object.md) | | An object with `"key": "value"` pairs that determine which loot table (`"key"`) will be replaced with a new loot table (`"value"`).
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the loot tables will only be replaced if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the loot tables will only be replaced if the block at the context of the loot tables fulfill this condition.
`item_condition` | [Item Condition Types](../item_condition_types.md) | _optional_ | If specified, the loot tables will only be replaced if the item in the context of the loot tables fulfill this condition.
`priority` | [Integer](../data_types/integer.md) | `0` | Determines the application priority of the power.


### Examples

`data/example/loot_tables/double_drops.json`

```json
{
    "type": "minecraft:block",
    "pools": [
        {
            "rolls": 2,
            "entries": [
                {
                    "type": "minecraft:loot_table",
                    "name": "apoli:replaced_loot_table"
                }
            ]
        }
    ]
}
```

`data/example/powers/double_ores_except_diamond_ore.json`

```json
{
    "type": "origins:replace_loot_table",
    "replace": {
        "([a-z|0-9|\\-|_]).*:blocks\/((?!diamond).*)_ore": "example:double_drops"
    }
}
```

This example will essentially double the drops of Ore blocks except for Diamond Ore block, as indicated in the specified regular expression. The `apoli:replaced_loot_table` loot table contains the contents of the replaced loot table, which is in this case would be the loot tables for Ore blocks except for the Diamond Ore block.
<br>

`data/example/loot_tables/entities/custom_creeper_loot.json`

```json
{
    "type": "minecraft:entity",
    "pools": [
        {
            "rolls": 1,
            "entries": [
                {
                    "type": "minecraft:tag",
                    "name": "minecraft:creeper_drop_music_discs",
                    "expand": true
                }
            ]
        }
    ]
}
```

`data/example/powers/modify_creeper_loot.json`

```json
{
    "type": "origins:replace_loot_table",
    "replace": {
        "minecraft:entities/creeper": "example:entities/custom_creeper_loot"
    },
    "condition": {
        "type": "origins:equipped_item",
        "equipment_slot": "mainhand",
        "item_condition": {
            "type": "origins:ingredient",
            "ingredient": {
                "item": "minecraft:wooden_sword"
            }
        }
    }
}
```

This example will replace the loot table for Creepers with the `example:entities/custom_creeper_loot` loot table if the actor entity is holding a Wooden Sword, which will make the Creeper drop one of the Music Disc items from the `#minecraft:creeper_drop_music_discs` item tag in a random fashion if killed.
