---
title: Origin JSON
date: 2021-04-05
---
# Origin JSON Format

This is the format of a JSON file describing an origin. They need to be placed inside the `origins` folder within your namespace.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`powers` | [Array](data_types/array.md) of [Identifiers](data_types/identifier.md) | _optional_ | IDs of the powers this origin should have.
`icon` | [Item Stack](data_types/item_stack.md) | _optional_ | The item stack which is displayed as the icon for the origin in the top-left corner of the choose/view origin screen.
`unchoosable` | [Boolean](data_types/boolean.md) | false | If set to true, this origin will not show up in any origin layer to choose it, but it will still be able to be set for that layer with a command or via an origin upgrade.
`order` | [Integer](data_types/integer.md) | _optional_ | Specifies the position of this origin in the choose origin screen among the other origins with the same impact in the layer. If not specified, will be a really large number - basically adding it in the end.
`impact` | [Integer](data_types/integer.md) | 0 | Specifies the impact of this origin with a number from 0 (none) to 3 (high).
`name` | [String](data_types/string.md) | _optional_ | The display name of the origin. Can be a translation key which is localized in a language file, or the literal display name.
`description` | [String](data_types/string.md) | _optional_ | The description of the origin. Can be a translation key which is localized in a language file, or the literal description.
`upgrades` | [Array](data_types/array.md) of [Upgrades](upgrade_json.md) | _optional_ | A list of upgrades for this origin, specifying which advancements turn this origin into which other origin.
`loading_priority` | [Integer](data_types/integer.md) | 0 | Specifies when this origin is loaded. Higher numbers mean it's loaded later, which means it will override those with lower loading priorities which share the same ID.
