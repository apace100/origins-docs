---
title: Consume (Item Action Type)
date: 2021-04-04
---

# Consume

[Item Action Type](../item_action_types.md)

Removes a provided amount of items from the item stack.

Type ID: `origins:consume`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`amount` | [Integer](../data_types/integer.md) | `1` | The amount of items to remove.


### Example

```json
"item_action": {
    "type": "origins:consume",
    "amount": 1
}
```