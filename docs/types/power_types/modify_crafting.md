---
title: Modify Crafting (Power Type)
date: 2021-10-02
---

# Modify Crafting

[Power Type](../power_types.md)

Modifies the result item of a recipe using an [Item Action Type](../item_action_types.md) or an [Item Stack](../data_types/item_stack.md). It can also execute an [Entity Action Type](../entity_action_types.md) on the player and a [Block Action](../block_action_types.md) at the block used for crafting the recipe.

Type ID: `origins:modify_crafting`

!!! caution

    This power type **cannot** modify the result item from recipes added by the [Recipe (Power Type)](recipe.md).


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`recipe` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, modifies the result item of the recipe that matches the specified namespace and ID.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the item from the `result` field and the specified actions will only be applied if this condition is fulfilled by the result item of a recipe.
`result` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item will replace the item of a recipe.
`item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the result item of a recipe.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player upon crafting a recipe.
`block_action` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this action will be executed on the block used for crafting a recipe.


### Examples

```json
{
    "type": "origins:modify_crafting",
    "recipe": "minecraft:wooden_sword",
    "result": {
        "item": "minecraft:diamond_sword"
    }
}
```

This example will replace the result item stack from the `minecraft:wooden_sword` (`data/minecraft/recipes/wooden_sword.json`) vanilla recipe with a Diamond Sword only for the player that has the power.
