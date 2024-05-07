---
title: Multiple (Power Type)
date: 2021-04-07
---

# Multiple

[Power Type](../power_types.md)

Allows for defining more than one power in a single file.

Type ID: `origins:multiple`


!!! note

    The sub-powers are automatically hidden. When the super-power (where the `origins:multiple` power type is used) is added to the entity, all sub-powers are added automatically.


!!! note

    You can reference sub-powers by using the ID of the super-power and the ID of the sub-power, split by an underscore (`_`).
    (e.g: `namespace:super-power_sub-power`)


!!! caution

    If you wish to check for an entity condition for the entire super-power, you would have to check for the said entity condition in every sub-power of the super-power.


### Fields

Arbitrary fields. Any "key", except for `type`, `loading_priority`, `name`, `description`, `hidden`, `condition`, and `fabric:load_conditions`, is considered a sub-power and takes a fully-defined power type as the value.


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

This example super-power has two "keys", which are considered sub-powers: `toggle` and `invisibility`. The `invisibility` sub-power will only be active *(e.g: make the entity invisible)* if the `toggle` sub-power is toggled ON.
