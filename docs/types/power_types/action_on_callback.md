---
title: Action On Callback (Power Type)
date: 2021-05-25
---

# Action On Callback

[Power Type](../power_types.md)

Execute [Entity Action Types](../entity_action_types.md) depending on the context.

Type ID: `origins:action_on_callback`

!!! note

    For example: when the player chooses an origin that has the power, when the player joins the world, when the player leaves the world, when the player respawns or when the player becomes another origin.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action_chosen` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the player chooses their origin on the last layer through the menu - by using the Orb of Origin or missing an origin or joining for the first time - if the power was gained from any of the layers.
`execute_chosen_when_orb` | [Boolean](../data_types/boolean.md) | `true` | When this is false, the `entity_action_chosen` will not be executed when the player changes their origin with an orb, but only when the player chooses an origin for the first time or their origin was reset to `origins:empty` via a command.
`entity_action_lost` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is lost.
`entity_action_added` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is added. Joining a world adds each power back.
`entity_action_removed` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is removed and right after the player respawns. Leaving a world removes each power.
`entity_action_respawned` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player right after the player respawns, after the `entity_action_removed`.


### Examples

```json
{
  	"type": "origins:action_on_callback",
  	"entity_action_chosen": {
    	"type": "origins:execute_command",
    	"command": "team join TheNetherBoys @s"
  	},
  	"entity_action_lost": {
    	"type": "origins:execute_command",
    	"command": "team leave @s"
  	},
  	"execute_chosen_when_orb": true
}
```

This example will make players automatically join the team called "TheNetherBoys" upon choosing the origin that has the power, and will make the players also leave automatically if they ever change their origin with another one that doesn't have the power.
(The "TheNetherBoys" team has to exist beforehand for this power to work!)
