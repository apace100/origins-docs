---
title: Selector Action (Entity Action Type)
date: 2023-05-21
---

# Selector Action

[Entity Action Type](../entity_action_types.md)

Executes an action on entities selected by a target selector.

Type ID: `origins:selector_action`


!!! note

    See [Minecraft Wiki: Target selectors](https://minecraft.wiki/w/Target_selectors) for more information about target selectors.

!!! note

    This entity action type has a bi-entity action context, where the '**actor**' entity is the entity that invoked the entity action while the '**target**' entities are the entities that were selected by the specified `selector`.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`selector` | [String](../data_types/string.md) | | The selector to use for selecting entities. It can be the username of a player, the UUID of the entity or a target selector.
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either or both the '**actor**' and '**target**' entities.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified action will only be executed if this condition is fulfilled by either or both the '**actor**' and '**target**' entities.


### Examples

```json
"entity_action": {
    "type": "origins:selector_action",
    "selector": "Steve",
    "bientity_action": {
        "type": "origins:damage",
        "amount": 5,
        "damage_type": "minecraft:generic"
    }
}
```

This example will deal 2 and a half hearts of damage to the player named Steve.
<br>

```json
"entity_action": {
    "type": "origins:selector_action",
    "selector": "@e[type = minecraft:armor_stand, tag = some_tag]",
    "bientity_action": {
        "type": "origins:target_action",
        "action": {
            "type": "origins:execute_command",
            "command": "kill @s"
        }
    }
}
```

This example will kill armor stands that have the `some_tag` tag *(added via the `/tag` command)*
