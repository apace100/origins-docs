---
title: Action On Callback (Power Type)
date: 2021-05-25
---

# Action On Callback

[Power Type](../power_types.md)

Execute [Entity Action Types](../entity_action_types.md) depending on the context.

Type ID: `apoli:action_on_callback`

!!! note

    For example: when the player joins the world, when the player leaves the world or when the player respawns.

### Fields

| Field                     | Type                                            | Default    | Description                                                                                                                                                 |
| ------------------------- | ----------------------------------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `entity_action_lost`      | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is lost.                                                                            |
| `entity_action_added`     | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is added. Joining a world adds each power back.                                     |
| `entity_action_removed`   | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is removed and right after the player respawns. Leaving a world removes each power. |
| `entity_action_respawned` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player right after the player respawns, after the `entity_action_removed`.                                |

### Examples

```json
{
	"type": "apoli:action_on_callback",
	"entity_action_added": {
		"type": "apoli:execute_command",
		"command": "team join TheNetherBoys @s"
	},
	"entity_action_lost": {
		"type": "apoli:execute_command",
		"command": "team leave @s"
	}
>>>>>>> latest
}
```

This example will make players automatically join the team called "TheNetherBoys" upon getting the power, and will make the players also leave automatically if they ever get this power revoked.
(The "TheNetherBoys" team has to exist beforehand for this power to work!)
