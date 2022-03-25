---
title: Power JSON
date: 2021-04-07
---

# Power JSON Format

This is the format of a JSON file describing a power.

Power files need to be placed inside the `powers` folder within your namespace.

Depending on the chosen `type`, power JSONs have more required and optional fields. See the corresponding power type page for a description of what those fields are.

### Fields

| Field              | Type                                                   | Default    | Description                                                                                                                                                           |
| ------------------ | ------------------------------------------------------ | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `type`             | [Identifier](../types/data_types/identifier.md)        |            | The namespace and ID of the desired [Power Type](../types/power_types.md).                                                                                            |
| `name`             | [String](../types/data_types/string.md)                | _optional_ | The display name of the power. Can be a literal string or a translation key.                                                                                          |
| `description`      | [String](../types/data_types/string.md)                | _optional_ | The description of the power. Can be a literal string or a translation key.                                                                                           |
| `hidden`           | [Boolean](../types/data_types/boolean.md)              | `false`    | If set to true, this power will not be displayed.                                                                                     |
| `condition`        | [Entity Condition](../types/entity_condition_types.md) | _optional_ | If set, this power will only be active when the player with this power fulfills the condition.                                                                        |
| `loading_priority` | [Integer](../types/data_types/integer.md)              | `0`        | Specifies when this power is loaded. Higher numbers mean it's loaded later, which means it will override those with lower loading priorities which share the same ID. |

### Examples

```json
{
	"type": "apoli:active_self",
	"entity_action": {
		"type": "apoli:execute_command",
		"command": "tellraw @a {\"text\": \"Hello world!\", \"color\": \"green\"}"
	},
	"name": "Hello World!",
	"description": "A power that announces a 'Hello world!' message to everyone in the server."
}
```

This example will print a green-colored 'Hello world!' message to all currently online players once activated.
