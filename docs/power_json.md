---
title: Power JSON
date: 2021-04-07
---

# Power JSON Format

This is the format of a JSON file describing a power. Powers are used to give functionality to origins.

Power files need to be placed inside the `powers` folder within your namespace.

Depending on the chosen `type`, power JSONs have more required and optional fields. See the corresponding power type page for a description of what those fields are.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`type` | [Identifier](data_types/identifier.md) | | ID of the desired [Power Type](power_types.md).
`name` | [String](data_types/string.md) | _optional_ | The display name of the power. Can be a literal string or a translation key.
`description` | [String](data_types/string.md) | _optional_ | The description of the power. Can be a literal string or a translation key.
`hidden` | [Boolean](data_types/boolean.md) | false | If set to true, this power will not be displayed in the power list of the origin.
`condition` | [Entity Condition](entity_conditions.md) | _optional_ | If set, this power will only be active when the player with this power fulfills the condition.
`loading_priority` | [Integer](data_types/integer.md) | 0 | Specifies when this power is loaded. Higher numbers mean it's loaded later, which means it will override those with lower loading priorities which share the same ID.
`badges` | [Array](data_types/array.md) of [Badges](data_types/badge.md) | _optional_ | If set, it will display icon(s) after the name of the power.

### Example
```json
{
    "type": "origins:active_self",
    "entity_action": {
        "type": "origins:execute_command",
        "command": "tellraw @a {\"text\": \"Hello world!\", \"color\": \"green\"}"
    },
    "name": "Hello World!",
    "description": "A power that announces a 'Hello world!' message to everyone in the server.",
    "badges": [
        {
            "sprite": "minecraft:textures/item/diamond.png",
            "text": "Ooh, shiny!"
        }
    ]
}
```
This example power will print a green-colored 'Hello world!' message to all currently online players once activated.