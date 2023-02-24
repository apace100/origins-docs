---
title: Stat (Data Type)
date: 2023-02-24
---

#   Stat

[Data Type](../data_types.md)

An [object](object.md) specifying a statistic via a statistic type and an [identifier](identifier.md).


!!! note

    See [Minecraft Fandom Wiki: Statistic (Resource location)](https://minecraft.fandom.com/wiki/Statistics#Resource_location) for a list of vanilla statistic types and names.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`type` | [Identifier](identifier.md) | | The type of the statistic.
`id` | [Identifier](identifier.md) | | The name of the statistic; may depend on the specified type of the statistic.


### Examples

```json
"stat": {
    "type": "minecraft:custom",
    "id": "minecraft:time_since_rest"
}
```

This example specifies the statistic for tracking the time since the last time a player has rested.
<br>

```json
"stat": {
    "type": "minecraft:mined",
    "id": "minecraft:dirt"
}
```

This example specifies the statistic for tracking how much Dirt blocks a player has mined.
