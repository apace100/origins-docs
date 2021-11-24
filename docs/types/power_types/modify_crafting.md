---
title: Modify Crafting (Power Type)
date: 2021-10-02
---

# Modify Crafting

[Power Type](../power_types.md)

Modifies the result item of a recipe using an item action or an item stack. It also executes an entity action on the player and executes a block action in the block used for crafting the recipe.

Type ID: `origins:modify_crafting`

!!! caution

    This power type **cannot** modify the result item from recipes added by the [Recipe](recipe.md) power type.

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`recipe` | [Identifier](../types/data_types/identifier.md) | _optional_ | If specified, modifies the result item of the recipe that matches the specified namespace and ID.
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If specified, the item from the `result` field and the specified actions will only be applied if this condition is fulfilled by the result item of a recipe.
`result` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item will replace the item of a recipe.
`item_action` | [Item Action](../item_actions.md) | _optional_ | If specified, this action will be executed on the result item of a recipe.
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If specified, this action will be executed on the player upon crafting a recipe.
`block_action` | [Block Action](../block_actions.md) | _optional_ | If specified, this action will be executed on the block used for crafting a recipe.

### Example
```json
{
    "type": "origins:modify_crafting",
    "recipe": "minecraft:wooden_sword",
    "result": {
        "item": "minecraft:diamond_sword"
    }
}
```
This example replaces the result item stack from the `minecraft:wooden_sword` (`data/minecraft/recipes/wooden_sword.json`) vanilla recipe with a Diamond Sword.