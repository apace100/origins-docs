---
title: Play Sound (Action)
date: 2021-04-05
---
# Play Sound

[Entity Action](../entity_actions.md).

Plays a sound at the entity's position. Currently only works on player entities.

Type ID: `origins:play_sound`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`sound` | [Identifier](../data_types/identifier.md) | | ID of the sound to play.
`volume` | [Float](../data_types/float.md) | 1 | The volume of the sound.
`pitch` | [Float](../data_types/float.md) | 1 | The pitch of the sound.


### Example
```json
"entity_action": {
  "type": "origins:play_sound",
  "sound": "minecraft:entity.chicken.egg"
}
```
Plays the sound of a chicken laying an egg at the entity's position.
