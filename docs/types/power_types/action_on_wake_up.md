---
title: Action On Wake Up (Power Type)
date: 2021-04-04
---

# Action On Wake Up

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) or a [Block Action type](../block_action_types.md) when the player wakes up after sleeping.

Type ID: `origins:action_on_wake_up`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player when they wake up.
`block_action` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this action will be executed on the bed block.
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the specified actions will only execute if this condition is fulfilled by the bed block.



### Examples

```json
{
    "type": "origins:action_on_wake_up",
    "entity_action": {
        "type": "origins:and",
        "actions": [
            {
                "type": "origins:execute_command",
                "command": "title @s actionbar {\"translate\": \"You feel %1$s but %2$s\", \"color\": \"yellow\", \"with\": [{\"text\": \"rejuvenated\", \"color\": \"green\"}, {\"text\": \"hungry...\", \"color\": \"red\"}]}"
            },
            {
                "type": "origins:apply_effect",
                "effects": [
                    {
                        "effect": "minecraft:regeneration",
                        "duration": 100,
                        "amplifier": 1,
                        "is_ambient": true,
                        "show_particles": true,
                        "show_icon": true
                    },
                    {
                        "effect": "minecraft:hunger",
                        "duration": 100,
                        "amplifier": 2,
                        "is_ambient": true,
                        "show_particles": true,
                        "show_icon": true
                    }
                ]
            }
        ]
    },
    "block_condition": {
        "type": "origins:block",
        "block": "minecraft:red_bed"
    }
}
```

This example will apply a Regeneration II and Hunger III status effect that both lasts for 5 seconds, and execute a `/title` command that will display a "`You feel rejuvenated but hungry...`" message in the actionbar if the player has woken up from sleeping in a Red Bed.
