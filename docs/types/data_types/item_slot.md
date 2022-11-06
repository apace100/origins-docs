---
title: Item Slot (Data Type)
date: 2022-11-06
---

#   Item Slot

[Data Type](../data_types.md)

A [string](string.md) that represents a slot from an entity or container's inventory.


!!! note

    It's recommended to use the `container.<slot_number>` item slots for representing the slots of a power that uses the [Inventory (Power Type)](../power_types/inventory.md)


### Table

Name                       | Valid `<slot_number>` | Mapped index
---------------------------|-----------------------|-------------
`armor.chest`              |                       | 102
`armor.feet`               |                       | 100
`armor.head`               |                       | 103
`armor.legs`               |                       | 101
`container.<slot_number>`  | 0 to 53               | 0 to 53
`enderchest.<slot_number>` | 0 to 26               | 200 to 226
`horse.<slot_number>`      | 0 to 14               | 500 to 514
`horse.armor`              |                       | 401
`horse.saddle`             |                       | 400
`hotbar.<slot_number>`     | 0 to 8                | 0 to 8
`inventory.<slot_number>`  | 0 to 26               | 9 to 35
`villager.<slot_number>`   | 0 to 7                | 300 to 307
`weapon.mainhand`          |                       | 98
`weapon.offhand`           |                       | 99
`weapon`                   |                       | 98


### Examples

```json
"slot": "weapon.mainhand"
```

This example represents the mainhand slot of the entity.
<br>

```json
"slots": [
    "container.0",
    "container.1",
    "container.2",
    "container.3",
    "container.4",
    "container.5",
    "container.6",
    "container.7",
    "container.8"
]
```

This example represents slots 0 to 8 of a container. It may be used to represent the hotbar slots 0 to 8 of a player, considering that the mappings have the same mapped index.
