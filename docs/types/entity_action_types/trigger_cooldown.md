---
title: Trigger Cooldown (Entity Action Type)
date: 2021-04-06
---

# Trigger Cooldown

[Entity Action Type](../entity_action_types.md)

Starts the cooldown of a power that uses a [Power Type](../power_types.md) that has a built-in cooldown, as if that power has just been used.

Type ID: `origins:trigger_cooldown`

!!! note

    Here's a list of power types that have built-in cooldowns:

    * [Action On Hit](../power_types/action_on_hit.md)
    * [Action When Damage Taken](../power_types/action_when_damage_taken.md)
    * [Action When Hit](../power_types/action_when_hit.md)
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
`power` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the power that will be triggered.


### Examples

```json
"entity_action": {
  	"type": "origins:trigger_cooldown",
  	"power": "origins:launch_into_air"
}
```

This example will trigger the cooldown of the 'Gift of the Winds' (`origins:launch_into_air` (`data/origins/powers/launch_into_air.json`)) power as if the entity had used that ability.
