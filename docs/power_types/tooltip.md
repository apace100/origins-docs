---
title: Tooltip (Power Type)
date: 2021-10-05
---

# Tooltip

[Power Type](../power_types.md)

Applies the specified tooltip(s) to an item that is only visible to the entity that has the power.

Type ID: `origins:tooltip`

!!! note

    The `text` and `texts` fields can accept [JSON text components](https://minecraft.fandom.com/wiki/Raw_JSON_text_format). However, JSON text components that needs to be resolved may **not work**.
    
### Fields

Field | Type | Default | Description
------|------|---------|-------------
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If specified, the specified tooltip(s) will only apply to items that fulfills this condition.
`text` | [String](../data_types/string.md) | _optional_ | If specified, apply this string as a tooltip.
`texts` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | _optional_ | If specified, apply these strings as a tooltip.

### Example
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
This example will apply a tooltip to an Egg item.