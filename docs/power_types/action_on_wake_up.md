---
title: Action On Wake Up (Power Type)
date: 2021-04-04
---
# Action On Wake Up

[Power Type](../power_types.md).

Executes an entity action or a block action when the player wakes up after sleeping.

Type ID: `origins:action_on_wake_up`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player when they wake up.
`block_action` | [Block Action](../block_actions.md) | _optional_ | If set, this action will be executed on the bed block.
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | If set, the actions will only trigger when this block condition is met by the bed block.


### Example
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
This power will give the player a regeneration and hunger status effects, and run a `/title` command that displays a "`You feel rejuvenated but hungry...`" message in the actionbar if the player has woken up from sleeping in a red bed.