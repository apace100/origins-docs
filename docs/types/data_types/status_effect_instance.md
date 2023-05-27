---
title: Status Effect Instance (Data Type)
date: 2021-04-04
---

# Status Effect Instance

[Data Type](../data_types.md)

An [Object](object.md) used to define a status effect with duration, amplifier, etc.


!!! note

    To make the Status Effect Instance infinite, you can set the value of `duration` to `-1`.


### Fields

Field  | Type | Default | Description
-------|-----|---------------|-------------
`effect` | [Identifier](identifier.md) | | The identifier of the status effect.
`duration` | [Integer](integer.md) | `100` | Determines the duration of the status effect (in ticks).
`amplifier` | [Integer](integer.md) | `0` | Determines the strength of the status effect (0 being level 1).
`is_ambient` | [Boolean](boolean.md) | `false` | Determines whether the particle effects of the status effect is less noticable.
`show_particles` | [Boolean](boolean.md) | `true` | Determines whether the status effect should display particle effects on the entity.
`show_icon` | [Boolean](boolean.md) | `true` | Determines whether the status effect would display an icon on the HUD.


### Examples

```json
"effect": {
    "effect": "minecraft:slowness",
    "amplifier": 1,
    "duration": -1
}
```

A Slowness II status with an infinite (∞) duration.
<br>

```json
"effect": {
    "effect": "minecraft:levitation",
    "duration": 200,
    "is_ambient": true,
    "show_particles": true,
    "show_icon": false
}
```

An ambient and mostly hidden status effect of Levitation I which lasts for 10 seconds.
<br>

```json
"effects": [
    {
        "effect": "minecraft:slow_falling",
        "duration": 400,
        "is_ambient": false,
        "show_particles": false,
        "show_icon": true
    },
    {
        "effect": "minecraft:slowness",
        "duration": 400,
        "is_ambient": false,
        "show_particles": false,
        "show_icon": true
    }
]
```
An [Array](array.md) of status effect instances with the Slowness I and Slow Falling I status effects that lasts for 20 seconds
