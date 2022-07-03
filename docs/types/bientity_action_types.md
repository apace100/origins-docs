---
title: Bi-entity Action Types
date: 2021-10-06
---

# Bi-entity Action Types

Bi-entity Action Types operate on a `Pair<Entity, Entity>`; in simpler terms: an actor and a target. The actor and target is determined depending on the used power type, and can be swapped using [Invert](bientity_action_types/invert.md). These are available to power/action types that provides a `bientity_action` object field.

As a rule of thumb, the actor is usually the entity that "triggers" the action (e.g. uses or attacks another entity), while the target is the entity that is being targeted (e.g. the entity that is being used or attacked).


### List

* [Add Velocity](bientity_action_types/add_velocity.md)
* [Damage](bientity_action_types/damage.md)
* [Mount](bientity_action_types/mount.md)
* [Set In Love](bientity_action_types/set_in_love.md)
* [Tame](bientity_action_types/tame.md)


### Meta
* [Actor Action](bientity_action_types/actor_action.md)
* [Invert](bientity_action_types/invert.md)
* [Target Action](bientity_action_types/target_action.md)
