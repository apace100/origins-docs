---
title: Attacker Action When Hit (Power Type)
date: 2021-04-03
---
# Attacker Action When Hit

[Power Type](../power_types.md).

Executes an entity action on the attacker when the player is hit by another entity.

Type ID: `origins:attacker_action_when_hit`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | | The action to execute on the attacker.
`cooldown` | [Integer](../data_types/integer.md) | | Interval of ticks this power needs to recharge before the action can be executed again.
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If set, the action will only trigger when this condition holds for the damage that was dealt by the attacker.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | If set, the cooldown of this power is visualized on the HUD in the specified way.

### Example

```json
{
  "type": "origins:attacker_action_when_hit",
  "entity_action": {
    "type": "origins:add_velocity",
    "y": 2
  },
  "cooldown": 20
}
```
When a mob or player attacks a player with this power, they will get thrown upwards into the air.
