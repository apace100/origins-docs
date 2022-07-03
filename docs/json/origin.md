---
title: Origin JSON
date: 2021-04-05
---

# Origin JSON Format

This is the format of a JSON file describing an origin. Origins are used to give players special abilities, which can alter the player's gameplay.

Origin JSON files need to be placed inside the `data/<namespace>/origins` folder of your datapack. The said files can be referenced as `namespace:path/to/origin` (`data/namespace/origins/path/to/origin.json`) in the `origins` field of an [Origin Layer (JSON)](origin_layer.md) file.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`powers` | [Array](../types/data_types/array.md) of [Identifiers](../types/data_types/identifier.md) | _optional_ | The namespace and IDs of the powers this origin should have.
`icon` | [Item Stack](../types/data_types/item_stack.md) | _optional_ | The item stack which is displayed as the icon for the origin in the top-left corner of the choose/view origin screen.
`unchoosable` | [Boolean](../types/data_types/boolean.md) | `false` | If set to true, this origin will not show up in any origin layer to choose it, but it will still be able to be set for that layer with a command or via an origin upgrade.
`order` | [Integer](../types/data_types/integer.md) | _optional_ | Specifies the position of this origin in the choose origin screen among the other origins with the same impact in the layer. If not specified, will be a really large number - basically adding it in the end.
`impact` | [Integer](../types/data_types/integer.md) | `0` | Specifies the impact of this origin with a number from 0 (none) to 3 (high).
`name` | [String](../types/data_types/string.md) | _optional_ | The display name of the origin. Can be a translation key which is localized in a language file, or the literal display name.
`description` | [String](../types/data_types/string.md) | _optional_ | The description of the origin. Can be a translation key which is localized in a language file, or the literal description.
`upgrades` | [Array](../types/data_types/array.md) of [Upgrades](upgrade.md) | _optional_ | A list of upgrades for this origin, specifying which advancements turn this origin into which other origin.
`loading_priority` | [Integer](../types/data_types/integer.md) | `0` | Specifies when this origin is loaded. Higher numbers mean it's loaded later, which means it will override those with lower loading priorities which share the same ID.


### Examples

```json
{
    "powers": [],
    "icon": {
        "item": "minecraft:zombie_head"
    },
    "order": 3,
    "impact": 2,
    "name": "Zombie",
    "description": "Raah, brains..."
}
```

This example will add an origin that has a Zombie Head item as its icon.
