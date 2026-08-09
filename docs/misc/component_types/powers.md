---
title: Powers (Component Type)
date: 2026-04-23
---

#   Powers

[Component Type](../component_types.md)

Grants the entity the powers from a list of [objects](../../types/data_types/object.md) which contain the ID of the power, target slot, and other metadata whenever the item is equipped in the specified slot.

Type ID: `apoli:powers`

!!! note

    The field table below outlines the fields of the object to be contained by this component type.

!!! warning

    Currently, the data of powers granted by this component type does <span style="color:darkred"><b>NOT</b></span> persist in the item stacks that have the component.


### Fields

Field       |   Type                                                                            |   Default |   Description
------------|-----------------------------------------------------------------------------------|-----------|--------------
`power`     |   [Identifier](../../types/data_types/identifier.md)                              |           |   The ID of the power that will be granted.
`slot`      |   [Attribute Modifier Slot](../../types/data_types/attribute_modifier_slot.md)    |           |   The target slot for the power.
`hidden`    |   [Boolean](../../types/data_types/boolean.md)                                    |   `false` |   Determines whether the power should be hidden in the tooltip.
`negative`  |   [Boolean](../../types/data_types/boolean.md)                                    |   `false` |   Determines whether the color of the power's name in the tooltip should be yellow (`false`) or red (`true`).


### Examples

```mcfunction
give @s minecraft:leather_chestplate[apoli:powers = [{power: "origins:arcane_skin", slot: "chest"}]]
```
This example will define an `apoli:powers` component to a Leather Chestplate, which will grant the `origins:arcane_skin` power to the entity if the said item is worn in the chest slot.
<br>

```mcfunction
give @s minecraft:iron_sword[apoli:powers = [{power: "origins:fragile", slot: "hand", negative: true}, {power: "origins:like_air", slot: "hand"}]]
```
This example will define an `apoli:powers` component to an Iron Sword, which will grant the `origins:fragile` and `origins:like_air` powers if the item is held in either the mainhand or the offhand, with the `origins:fragile` power having a red name tooltip.
