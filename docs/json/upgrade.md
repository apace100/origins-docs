---
title: Upgrade JSON
date: 2021-04-05
---

# Upgrade JSON Format

An [Object](../types/data_types/object.md) used to specify an upgrade of an origin within an [Origin JSON](origin.md).


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Identifier](../types/data_types/identifier.md) | | ID of an advancement which should trigger this upgrade.
`origin` | [Identifier](../types/data_types/identifier.md) | | ID of an origin the origin with this upgrade should upgrade to.
`announcement` | [String](../types/data_types/string.md) | _optional_ | A text which will show up in the local chat of the player in a pretty color. If none is specified, there won't be a message.

### Example
```json
"upgrades": [
    {
        "condition": "minecraft:end/kill_dragon",
        "origin": "origins:elytrian",
        "announcement": "You have killed an ender dragon! You have evolved to Elytrian"
    }
]
```
This example will change the player's origin to `origins:elytrian` once they've killed an ender dragon (or when they've been granted the `minecraft:end/kill_dragon` advancement).