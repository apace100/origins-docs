---
title: Text Component (Data Type)
date: 2022-07-03
---

#   Text Component

[Data Type](../data_types.md)

A [String](string.md) or [Object](object.md) used for displaying text with fancy formatting.

!!! note

    You can refer to [Minecraft Fandom: Raw JSON text format](https://minecraft.fandom.com/wiki/Raw_JSON_text_format) for JSON text components you can use.


### Examples

```json
"text": "This is an example text string!"
```

This example will display a text that says "`This is an example text string!`".
<br>

```json
"text": {
    "text": "This is an example text string with a fancy color!",
    "color": "yellow"
}
```

This example will display a yellow-colored text that says "`This is an example text string with a fancy color!`"
<br>

```json
"text": [
    "This is an example text string with a translated keybind (",
    {
        "keybind": "key.attack"
    },
    ") using the 'keybind' JSON text component!"
]
```

This example will display a text that'd say "`This is an example text string with a translated keybind (<keybind>) using the 'keybind' JSON text component`", with `<keybind>` being the translated name of the `key.attack` keybind.
