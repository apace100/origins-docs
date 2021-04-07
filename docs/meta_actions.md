---
title: Meta Actions
date: 2021-04-07
---
# Meta Actions

Meta Actions are independent of the type they operate on. They basically combine or modify other actions. The actions which are modified have to be of the type the field of the meta_action requires. For example, if you have a field which requires an [Entity Action](entity_actions.md) and you insert a [Delay](delay) meta action, the action you need to provide inside that action will have to be an [Entity Action](entity_actions.md) as well.

## List

* [And](and)
* [Chance](chance)
* [Choice](choice)
* [Delay](delay)*
* [If-Else](if_else)
* [If-Else List](if_else_list)*

*: These actions are currently only available as [Entity Actions](entity_actions.md).
