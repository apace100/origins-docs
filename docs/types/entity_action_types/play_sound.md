---
title: Play Sound (Entity Action Type)
date: 2021-04-05
---

# Play Sound

[Entity Action Type](../entity_action_types.md)

Plays a sound event at the entity's position. Currently only works on player entities.

Type ID: `apoli:play_sound`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`sound` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the sound to play.
`volume` | [Float](../data_types/float.md) | `1` | The volume of the sound.
`pitch` | [Float](../data_types/float.md) | `1` | The pitch of the sound.



### Examples
```json
"entity_action": {
    "type": "apoli:play_sound",
    "sound": "minecraft:entity.chicken.egg"
}
```

This example will play the `minecraft:entity.chicken.egg` sound event at the entity's position.
