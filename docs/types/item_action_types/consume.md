---
title: Consume (Item Action Type)
date: 2021-04-04
---

# Consume

[Item Action Type](../item_action_types.md)

Removes a provided amount of items from the item stack.

Type ID: `apoli:consume`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`amount` | [Integer](../data_types/integer.md) | `1` | The amount of items to remove.



### Examples

```json
"item_action": {
    "type": "apoli:consume",
    "amount": 1
}
```

This example will "consume" (remove) 1 item from the item stack.