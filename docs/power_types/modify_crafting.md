---
title: Modify Crafting (Power Type)
date: 2021-10-02
---
# Modify Crafting

[Power Type](../power_types.md)

Modifies the result item of a recipe using an item action or an item stack. It also executes an entity action on the player and executes a block action in the block used for crafting the recipe.

Type ID: `origins:modify_crafting`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`recipe` | [Identifier](../data_types/identifier.md) | _optional_ | The ID of the recipe to be modified.
`item_condition"` | [Item Condition](../item_conditions.md) | _optional_ | If set, it will only apply the item stack from the `result` field, and trigger the actions when this condition is met by the result item from the crafting recipe.
`result` | [Item Stack](../data_types/item_stack.md) | _optional_ | If set, replaces the result item stack of the recipe.
`item_action` | [Item Action](../item_actions.md) | _optional_ | If set, execute this item action on the result item stack.
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, execute this entity action on the player.
`block_action` | [Block Action](../block_actions.md) | _optional_ | If set, execute this block action at the block used for crafting the recipe.

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