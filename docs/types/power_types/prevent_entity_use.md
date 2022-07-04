---
title: Prevent Entity Use (Power Type)
date: 2021-10-06
---

# Prevent Entity Use

[Power Type](../power_types.md)

Prevents the player that has the power from "using" (right-clicking) an entity and executes a bi-entity action, item action and/or give an item upon being prevented.

Type ID: `origins:prevent_entity_use`

!!! note

    In the context of this power type, the '**actor**' entity is the entity that has the power whilst the '**target**' entity is the entity that was "used" (right-clicked).


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either or both the '**actor**' and '**target**' entities.
`held_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item used by the '**actor**' entity for right-clicking the '**target**' entity.
`result_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item that is given to the '**actor**' entity.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if this condition is fulfilled by the item used by the '**actor**' entity for right-clicking the '**target**' entity.
`hands` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]` | Determines if the power should be activated if the '**actor**' entity used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item stack will be given to the '**actor**' entity.


### Examples

```json
{
    "type": "origins:prevent_entity_use",
    "bientity_action": {
        "type": "origins:actor_action",
        "action": {
            "type": "origins:execute_command",
            "command": "title @s actionbar {\"text\": \"Cannot interact with pigs!\", \"color\": \"red\"}"
        }
    },
    "bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:pig"
        }
    }
}
```

This example will prevent the player that has the power from interacting with a Pig (also prevent powers that enables you to interact with a Pig) and executes an [Execute Command (Entity Action Type)](../entity_action_types/execute_command.md) to the entity that has attempted to interact with a Pig.
