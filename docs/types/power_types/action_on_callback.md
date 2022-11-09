---
title: Action On Callback (Power Type)
date: 2021-05-25
---

# Action On Callback

[Power Type](../power_types.md)

Execute [Entity Action Types](../entity_action_types.md) depending on the context.

Type ID: `origins:action_on_callback`

!!! note

    Callbacks may refer to when the player joins the world, when the player leaves the world, when the player respawns or when the player chooses an origin.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action_chosen` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player after the player finishes choosing an origin.
`execute_chosen_when_orb` | [Boolean](../data_types/boolean.md) | `true` | Determines whether the action in `entity_action_chosen` should be executed if the player also used an Orb of Origin item for choosing an origin.
`entity_action_gained` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is granted for the first time.
`entity_action_lost` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is removed permanently.
`entity_action_added` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is added. Joining a world adds each power back.
`entity_action_removed` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when the power is removed and right after the player respawns. Leaving a world removes each power.
`entity_action_respawned` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player right after the player respawns. This action will be executed after the action in `entity_action_removed`.


### Examples

```json
{
    "type": "origins:action_on_callback",
    "entity_action_chosen": {
        "type": "origins:apply_effect",
        "effect": {
            "effect": "minecraft:luck",
            "duration": 24000
        }
    },
    "execute_chosen_when_orb": false
}
```

This example will give the player the Luck I (30:00) status effect the moment the player has chosen the origin that has the power, unless the player used the Orb of Origin item to choose that origin.
<br>


```json
{
  	"type": "origins:action_on_callback",
  	"entity_action_gained": {
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

This example will make players automatically join the team called "TheNetherBoys" upon gaining the power, and will make the players also leave automatically if they ever change their origin with another one that doesn't have the power.
(The "TheNetherBoys" team has to exist beforehand for this power to work!)
