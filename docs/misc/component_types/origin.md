---
title: Origin (Component Type)
date: 2026-04-23
---

#   Origin

[Component Type](../component_types.md)

Enables the player to choose from list of [objects](../../types/data_types/object.md) which contain the IDs of the origin and its origin layer when the item is used.

Type ID: `origins:origin`

!!! note

    The field table below outlines the fields of the object to be contained by this component type.


### Fields

Field       |   Type                                                |   Default     |   Description
------------|-------------------------------------------------------|---------------|--------------
`layer`     |   [Identifier](../../types/data_types/identifier.md)  |               |   The ID of the origin layer to be selected.
`origin`    |   [Identifier](../../types/data_types/identifier.md)  |   _optional_  |   If specified, this origin will be automatically set to the specified origin layer.


### Examples

```mcfunction
give @s minecraft:stick[origins:origin = []]
```
This example will define an `origins:origin` component to a Stick item that enables the player to select from all the available and enabled origin layers when the item is used.
<br>

```mcfunction
give @s origins:orb_of_origin[origins:origin = [{layer: "origins:origin"}, {layer: "example:hello_world"}]]
```
This example will define an `origins:origin` component to an Orb of Origins item that enables the player to only select an origin from the defined origin layers (`origins:origin` and `example:hello_world`) when the item is used.
<br>

```mcfunction
give @s minecraft:egg[origins:origin = [{layer: "origins:origin", origin: "origins:arachnid"}]]
```
This example will define an `origins:origin` component to an Egg item that will automatically set the origin of the player in the `origins:origin` origin layer to `origins:arachnid` origin.
