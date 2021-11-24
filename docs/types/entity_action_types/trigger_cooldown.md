---
title: Trigger Cooldown (Entity Action Type)
date: 2021-04-06
---

# Trigger Cooldown

[Entity Action Type](../entity_action_types.md)

Starts the cooldown of a cooldown power, as if that power has just been used.

Type ID: `origins:trigger_cooldown`

!!! note

    Here's a list of power types that have built-in cooldowns:

    * [Active Self](../power_types/active_self.md)
    * [Attacker Action When Hit](../power_types/attacker_action_when_hit.md)
    * [Cooldown](../power_types/cooldown.md)
    * [Fire Projectile](../power_types/fire_projectile.md)
    * [Launch](../power_types/launch.md)
    * [Self Action On Hit](../power_types/self_action_on_hit.md)
    * [Self Action On Kill](../power_types/self_action_on_kill.md)
    * [Self Action When Hit](../power_types/self_action_when_hit.md)
    * [Target Action On Hit](../power_types/target_action_on_hit.md)

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`power` | [Identifier](../data_types/identifier.md) | | ID of the cooldown power which should trigger.

### Example
```json
"entity_action": {
  	"type": "origins:trigger_cooldown",
  	"power": "origins:launch_into_air"
}
```
Starts the cooldown of Gift of the Winds as if the player had used that ability.
