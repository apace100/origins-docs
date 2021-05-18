---
title: Positioned Item Stack Slots
date: 2021-05-15
---
# Positioned Item Stack Slots

An [Integer](../data_types/integer.md) that specifies the position (or slot) of a positioned item stack.


### Equipment Slots

  Slot  |  `/replaceitem` Slot  |  `Inventory` NBT Slot  
--------|-----------------------|-------------------------
  `40`  |  `weapon.offhand`     |  `-106b`
  `39`  |  `armor.head`         |  `103b`
  `38`  |  `armor.chest`        |  `102b`
  `37`  |  `armor.leggings`     |  `101b`
  `36`  |  `armor.boots`        |  `100b`

<br>


### Inventory Slots

  Slot  |  `/replaceitem` Slot  |  `Inventory` NBT Slot  
--------|-----------------------|-------------------------
  `35`  |  `inventory.26`       |  `35b`
  `34`  |  `inventory.25`       |  `34b`
  `33`  |  `inventory.24`       |  `33b`
  `32`  |  `inventory.23`       |  `32b`
  `31`  |  `inventory.22`       |  `31b`
  `30`  |  `inventory.21`       |  `30b`
  `29`  |  `inventory.20`       |  `29b`
  `28`  |  `inventory.19`       |  `28b`
  `27`  |  `inventory.18`       |  `27b`
  `26`  |  `inventory.17`       |  `26b`
  `25`  |  `inventory.16`       |  `25b`
  `24`  |  `inventory.15`       |  `24b`
  `23`  |  `inventory.14`       |  `23b`
  `22`  |  `inventory.13`       |  `22b`
  `21`  |  `inventory.12`       |  `21b`
  `20`  |  `inventory.11`       |  `20b`
  `19`  |  `inventory.10`       |  `19b`
  `18`  |  `inventory.9`        |  `18b`
  `17`  |  `inventory.8`        |  `17b`
  `16`  |  `inventory.7`        |  `16b`
  `15`  |  `inventory.6`        |  `15b`
  `14`  |  `inventory.5`        |  `14b`
  `13`  |  `inventory.4`        |  `13b`
  `12`  |  `inventory.3`        |  `12b`
  `11`  |  `inventory.2`        |  `11b`
  `10`  |  `inventory.1`        |  `10b`
  `9`   |  `inventory.0`        |  `9b`

<br>

### Hotbar Slots

  Slot  |  `/replaceitem` Slot  |  `Inventory` NBT Slot  
--------|-----------------------|-------------------------
  `8`   |  `hotbar.8`           |  `8b`
  `7`   |  `hotbar.7`           |  `7b`
  `6`   |  `hotbar.6`           |  `6b`
  `5`   |  `hotbar.5`           |  `5b`
  `4`   |  `hotbar.4`           |  `4b`
  `3`   |  `hotbar.3`           |  `3b`
  `2`   |  `hotbar.2`           |  `2b`
  `1`   |  `hotbar.1`           |  `1b`
  `0`   |  `hotbar.0`           |  `0b`

<br>

### Example:
```json
{
    "type": "origins:starting_equipment",
    "stacks": [
        {
            "item": "minecraft:white_stained_glass",
            "amount": 1,
            "slot": 39
        },
        {
            "item": "minecraft:leather_chestplate",
            "amount": 1,
            "tag": "{display: {color: 16383998}}",
            "slot": 38
        },
        {
            "item": "minecraft:leather_leggings",
            "amount": 1,
            "tag": "{display: {color: 16383998}}",
            "slot": 37
        },
        {
            "item": "minecraft:leather_boots",
            "amount": 1,
            "tag": "{display: {color: 16383998}}",
            "slot": 36
        },
        {
            "item": "minecraft:written_book",
            "amount": 1,
            "tag": "{display: {Name: '{\"text\": \"Example Book\", \"color\": \"light_purple\", \"italic\": false}'}, title: \"Example Book\", author: \"eggohito\", pages: ['{\"text\": \"This is page one.\"}', '{\"text\": \"This is page two, the last page.\"}']}",
            "slot": 8
        }
    ]
}
```
This example equips the player with a White Stained Glass on its head armor slot, a white-colored Leather Chestplate, Leggings and Boots for its chest, legs, and feet armor slots respectively, and a Written Book with two pages in the 9th hotbar slot.