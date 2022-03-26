---
title: String (Data Type)
date: 2021-04-04
---

# String

[Data Type](../data_types.md)

A piece of text. Has to be enclosed by quotation marks. Please note that if there are supposed to be quotation marks within the text itself, they need to be escaped with a backslash. (`\`)


### Examples

```json
{
	"field_name": "You should not sleep here!"
}
```

A simple text.
<br>

```json
{
	"type": "origins:execute_command",
	"command": "give @s minecraft:iron_axe{display:{Name:'{\"text\":\"Brutal Axe\", \"italic\": false}'}}"
}
```

A string to specify a command, which includes escaped quotation marks.