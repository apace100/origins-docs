---
title: Tooltip (Power Type)
date: 2021-10-05
---

# Tooltip

[Power Type](../power_types.md)

Applies the specified tooltip(s) to an item that is only visible to the entity that has the power.

Type ID: `origins:tooltip`


!!! warning

    Currently, this power type is not able to "resolve" certain JSON text components. See [Minecraft Fandom Wiki: Raw JSON text format (Component resolution)](https://minecraft.fandom.com/wiki/Raw_JSON_text_format#Component_resolution) for more information.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified tooltip(s) will only apply to items that fulfills this condition.
`text` | [Text Component](../data_types/text_component.md) | _optional_ | If specified, apply this string as a tooltip.
`texts` | [Array](../data_types/array.md) of [Text Components](../data_types/text_component.md) | _optional_ | If specified, apply these strings as a tooltip.
`order` | [Integer](../data_types/integer.md) | `0` | Determines the placement order of the tooltip(s) of the power.


### Examples

```json
{
    "type": "origins:tooltip",
    "item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:egg"
        }
    },
    "text": "Hmm, egg."
}
```

This example will apply a "`Hmm, egg.`" tooltip to an Egg item.
<br>

```json
{
    "type": "origins:tooltip",
    "item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:cake"
        }
    },
    "text": {
        "text": "Happy birthday!",
        "color": "yellow"
    }
}
```

This example will apply a yellow-colored "`Happy birthday!`" tooltip to a Cake item.
