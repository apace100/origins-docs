---
title: Swimming (Power Type)
date: 2021-04-08
---
# Swimming

[Power Type](../power_types.md).

Allows the player to swim (outside of water!).

Type ID: `origins:swimming`

### Fields

_None._


### Example
```json
{
    "type": "origins:swimming",
    "condition": {
        "type": "origins:on_block"
    }
}
```
This power will make the player swim instead of sprint if the player is on the ground.