---
title: Power Types
date: 2021-04-06
---
# Power Types

Powers are what grants functionality to your origins! Each power has a type, specified with
a `type` field in the JSON. Which type a power is defines which other fields it requires and supports.

Unless stated otherwise, each power type supports a `condition` field with an [entity condition](entity_conditions). See [Power JSON](power_json.md) for more details.

## Regular types

* [Attribute](attribute)
* [Conditioned Attribute](conditioned_attribute)
* [Burn](burn)
* [Cooldown](cooldown)
* [Effect Immunity](effect_immunity)
* [Elytra Flight](elytra_flight)
* [Multiple](multiple)
* [Simple](simple)
* [Toggle](toggle)

## Action-related

* [Action On Block Break](action_on_block_break)
* [Action On Callback](action_on_callback)
* [Action On Item Use](action_on_item_use)
* [Action On Land](action_on_land)
* [Action On Wake Up](action_on_wake_up)
* [Action Over Time](action_over_time)
* [Active Self](active_self)
* [Attacker Action When Hit](attacker_action_when_hit)
* [Self Action On Hit](self_action_on_hit)
* [Self Action On Kill](self_action_on_kill)
* [Self Action When Hit](self_action_when_hit)
* [Target Action On Hit](target_action_on_hit)

## Modifying types

* [Modify Break Speed](modify_break_speed)
* [Modify Damage Dealt](modify_damage_dealt)
* [Modify Damage Taken](modify_damage_taken)
* [Modify Exhaustion](modify_exhaustion)
* [Modify Food](modify_food)
* [Modify Harvest](modify_harvest)
* [Modify Jump](modify_jump)
* [Modify Lava Speed](modify_lava_speed)
* [Modify Player Spawn](modify_player_spawn)
* [Modify Swim Speed](modify_swim_speed)
* [Modify XP Gain](modify_xp_gain)

## Preventing types

* [Prevent Block Selection](prevent_block_selection)
* [Prevent Block Use](prevent_block_use)
* [Prevent Death](prevent_death)
* [Prevent Entity Render](prevent_entity_render)
* [Prevent Item Use](prevent_item_use)
* [Prevent Sleep](prevent_sleep)
