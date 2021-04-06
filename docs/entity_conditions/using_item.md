---
title: Using Item (Condition)
date: 2021-04-04
---
# Using Item

[Entity Condition](../entity_conditions.md).

Checks whether the player is using an item (holding right-click, as in drinking a potion or eating food).

Type ID: `origins:using_item`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If specified, the condition will only pass if the item that is being used fulfills this condition.

### Example:

```json
"condition": {
  "type": "origins:using_item",
  "item_condition": {
    "type": "origins:food"
  }
}
```
Checks whether the entity is currently eating food.
