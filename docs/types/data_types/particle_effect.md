---
title: Particle Effect
date: 2021-12-03
---

# Particle Effect

[Data Type](../data_types.md)

A data type that's either a [String](string.md) which defines only the particle type or an [Object](object.md) which defines the particle type and its additional parameters.


!!! note

    Refer to the [Minecraft Fandom Wiki: Particles (Particle IDs)](https://minecraft.fandom.com/wiki/Particles#Particle_IDs) page for a list of **vanilla** particle type IDs that you can use.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`type` | [Identifier](identifier.md) | | The namespace and ID of the particle type.
`params` | [String](string.md) | | The additional parameter for the particle type.


### Examples

```json
"particle": "minecraft:happy_villager"
```

A happy villager particle type.
<br>

```json
"particle": {
    "type": "minecraft:dust",
    "params": "0.922 0.314 0.314 2"
}
```

A red dust particle type with a count of 8.
<br>

```json
"particle": {
    "type": "minecraft:block",
    "params": "minecraft:ice"
}
```

A block particle type that uses the Ice texture.
