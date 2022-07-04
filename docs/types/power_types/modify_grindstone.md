---
title: Modify Grindstone (Power Type)
date: 2022-07-03
---

#   Modify Grindstone

[Power Type](../power_types.md)

Modifies the result of a certain item upon repairing/removing the enchantments of the said item using a Grindstone.

Type ID: `origins:modify_grindstone`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`result_type` | [Result Type](../data_types/result_type.md) | `"unchanged"` | Determines which item stack to use as a new result item stack.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player upon taking the item stack from the result slot of a Grindstone.
`block_action` | [Block Action Type](../block_action_types.md) | _optional_ | If specified, this action will be executed on the Grindstone block upon taking the item stack from the result slot of the said Grindstone block.
`item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the result item stack.
`item_action_after_grinding` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the result item stack **after** the grinding process.
`top_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if the item stack from the top input slot of the Grindstone fulfills this condition.
`bottom_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if the item stack from the bottom input slot of the Grindstone fulfills this condition.
`output_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if the item stack from the output/result slot of the Grindstone fulfills this condition.
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item stack will be used as a replacement only if the `result_type` field has a value of `"specified"`.
`xp_modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the value of the experience received from removing an enchantment from an item stack.


### Examples

```json
{
    "type": "origins:modify_grindstone",
    "xp_modifier": {
        "operation": "multiply_total_multiplicative",
        "value": 0.5
    }
}
```

This example will increase the experience recieved from removing enchantments from an enchanted item to 50%.
<br>

```json
{
    "type": "origins:modify_grindstone",
    "result_type": "specified",
    "block_action": {
        "type": "origins:set_block",
        "block": "minecraft:air"
    },
    "output_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:diamond_sword"
        }
    },
    "result_stack": {
        "item": "minecraft:netherite_sword"
    }
}
```

This example will replace the item in the output/result slot of a Grindstone with a Netherite Sword if the initial item is a Diamond Sword. This will also remove the used Grindstone block after taking the said item.
