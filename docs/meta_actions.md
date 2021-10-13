---
title: Meta Actions
date: 2021-04-07
---
# Meta Actions

Meta Actions are independent of the type they operate on. They basically combine or modify other actions. The actions which are modified have to be of the type the field of the meta_action requires. For example, if you have a field which requires an [Entity Action](entity_actions.md) and you insert a [Delay](delay) meta action, the action you need to provide inside that action will have to be an [Entity Action](entity_actions.md) as well.

## List

* [Actor Action](meta_actions/actor_action.md)\*\*
* [And](meta_actions/and.md)
* [Chance](meta_actions/chance.md)
* [Choice](meta_actions/choice.md)
* [Delay](meta_actions/delay.md)\*
* [If-Else List](meta_actions/if_else_list.md)\*
* [If-Else](meta_actions/if_else.md)
* [Invert](meta_actions/invert.md)\*\*
* [Nothing](meta_actions/nothing.md)\*\*\*
* [Target Action](meta_actions/target_action.md)\*\*

\*: These actions are currently only available as [Entity Actions](entity_actions.md).
<br>

\*\*: These actions are currently only available as [Bi-entity Actions](bientity_actions.md).
<br>

\*\*\*: These actions are currently only available as [Entity Actions](entity_actions.md) and [Bi-entity Actions](bientity_actions.md).
