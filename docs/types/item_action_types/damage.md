---
title: Damage (Item Action Type)
date: 2021-10-02
---

# Damage

[Item Action Type](../item_action_types.md)

Damages the item stack with a specified amount.

Type ID: `origins:damage`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`amount` | [Integer](../data_types/integer.md) | `1` | The amount of damage it should do to the item stack.
`ignore_unbreaking` | [Boolean](../data_types/boolean.md) | `false` | Determines if this action should ignore the Unbreaking enchantment.


### Example
```json
"item_action": {
    "type": "origins:damage",
    "amount": 10,
    "ignore_unbreaking": true
}
```
This example damages the item stack by 10, ignoring the Unbreaking enchantment.