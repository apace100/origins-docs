---
title: Prevent Sleep (Power Type)
date: 2021-04-07
---
# Prevent Sleep

[Power Type](../power_types.md).

Prevents sleeping and sends the player a message about why they can't sleep.

Type ID: `origins:prevent_sleep`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | If set, sleep will only be prevented if this condition holds for the bed.
`message` | [String](../data_types/string.md) | "origins.cant_sleep" | The message that will be shown when sleep is prevented this way. Can be a literal text or a translation key which will be localized using a language file.
`set_spawn_point` | [Boolean](../data_types/boolean.md) | false | If true, right-clicking the bed while sleeping is prevented with this power will still set the spawn point (similar to what happens when you right-click a bed while it's daytime).

### Example
```json
{
    "type": "origins:prevent_sleep",
	"message": "It's not hot enough for you to sleep",
    "condition": {
		"type": "origins:on_fire",
		"inverted": true
	}
}
```
This power prevents the player from sleeping unless they are burning.
