---
title: Multiple (Power Type)
date: 2021-04-07
---

# Multiple

[Power Type](../power_types.md)

Allows for defining more that one power in a single file.

Type ID: `origins:multiple`

!!! note

    The sub-powers are hidden by default. When the super-power (where the `origins:multiple` power type is in) is added to the entity, all sub-powers are added automatically.

!!! caution

    If you wish to check for an entity condition, you would have to check for the said entity condition in every sub-power inside the super-power.


### Fields

Arbitrary fields. Any "key" is considered a sub-power, and takes a fully-defined power type as the value. You can reference sub-powers by using the super-power ID, appended by an underscore (`_`) and lastly the sub-power ID (which is the key), i.e. `<namespace>:<powerfile>_<subpower>`


### Examples 

```json
{
    "type": "origins:multiple",
    "toggle": {
        "type": "origins:toggle",
        "active_by_default": false,
        "key": {
            "key": "key.origins.secondary_active"
        }
    },
    "invisibility": {
        "type": "origins:invisibility",
        "render_armor": false,
        "condition": {
            "type": "origins:power_active",
            "power": "*:*_toggle"
        }
    }
}
```

This example will grant the player that has the super-power to toggle invisibility by pressing the Secondary ability key.
