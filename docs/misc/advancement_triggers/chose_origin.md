---
title: Chose Origin (Criterion)
date: 2021-12-01
---

# Chose Origin

[Advancement Trigger](../advancement_triggers.md)

Triggers when a player chooses the specified origin.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`origin` | [Identifier](../../types/data_types/identifier.md) | | The namespace and ID of the origin that you want to check for.


### Examples

```json
{
    "criteria": {
        "chose_phantom": {
            "trigger": "origins:chose_origin",
            "conditions": {
                "origin": "origins:phantom"
            }
        }
    }
}
```

This example will be granted to players who have chosen the `origins:phantom` origin.
<br>

```json
{
    "parent": "minecraft:story/root",
    "display": {
        "icon": {
            "item": "minecraft:player_head",
            "nbt": "{SkullOwner: \"Steve\"}"
        },
        "title": "I am Human!",
        "description": "You chose the Human origin.",
        "announce_to_chat": true,
        "frame": "task",
        "show_toast": true
    },
    "criteria": {
        "chose_human": {
            "trigger": "origins:chose_origin",
            "conditions": {
                "origin": "origins:human"
            }
        }
    }
}
```

This example will be granted to players who have chosen the `origins:human` origin.
