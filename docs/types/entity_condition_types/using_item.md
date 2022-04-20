---
title: Using Item (Entity Condition Type)
date: 2021-04-04
---

# Using Item

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity is currently using an item (eating a food item, using a shield, drawing a bow, etc.) that fulfills the specified [Item Condition Type](../item_condition_types.md).

Type ID: `origins:using_item`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the condition will only evaluate to true if the item that is being used fulfills the specified item condition type.


### Examples

```json
"condition": {
    "type": "origins:using_item",
    "item_condition": {
        "type": "origins:food"
    }
}
```

This example will check if the entity is currently eating a food item.
