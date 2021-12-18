---
title: Meta Action Types
date: 2021-04-07
---

# Meta Action Types

Meta Action Types are independent of the type they operate on. They basically combine or modify other action types. The actions which are modified have to be of the type the field of the meta action type requires. For example, if you have a field which requires an [Entity Action Type](entity_action_types.md) and you insert a [Delay (Meta Action Type)](meta_action_types/delay.md), the action type you need to provide inside that meta action type will have to be an [Entity Action Type](entity_action_types.md) as well.


### List

* [And](meta_action_types/and.md)
* [Chance](meta_action_types/chance.md)
* [Choice](meta_action_types/choice.md)
* [If-Else-List](meta_action_types/if_else_list.md)
* [If-Else](meta_action_types/if_else.md)


## Bi-entity Actions

* [Actor Action](bientity_action_types/actor_action.md)
* [Invert](bientity_action_types/invert.md)
* [Target Action](bientity_action_types/target_action.md)

## Block Actions

* [Offset](block_action_types/offset.md)

## Entity Actions

* [Delay](meta_action_types/delay.md)

## Entity and Bi-entity Actions

* [Nothing](meta_action_types/nothing.md)
