---
title: Default Translatable Text Component (Data type)
date: 2023-12-22
---


#	Translatable Text Component

[Data Type](../data_types.md)

A [text component](text_component.md), where if the specified [text component](text_component.md) is a string, it will be treated as a translation key.


!!! note

    You can refer to [Minecraft Wiki: Raw JSON text format](https://minecraft.wiki/w/Raw_JSON_text_format) for JSON text components you can use.


###	Examples

```json
"text": "example.translation_key"
```

This example will display a text that says `"example.translation_key"`, which can be translated into something else using a language file in a resource pack.
<br>

```json
"text": {
	"translate": "example.translation_key"
}
```

An alternative version of the example above, using the `translate` JSON text component.
