---
title: Orb of Origin (Items)
date: 2021-11-22
---

# Orb of Origin

[Item](../items.md)

An item that can change the origin(s) of the player upon "use" (right-click).

By default, the Orb of Origins item doesn't have a crafting recipe and lets you pick an origin for every origin layer that's available. You can change either of these things by creating a recipe (JSON file) for the item, and giving the item a custom NBT respectively.

Item ID: `origins:orb_of_origin`


### Creating a custom recipe

You can use [this website](https://crafting.thedestruc7i0n.ca/) to easily create a recipe. To create a recipe for the Orb of Origins item using the website, you can follow these steps:

1. In the 'Ingredients' section on the right side, click on the 'Add Item' button.
2. Enter `Orb of Origin` inside the 'Name' text box and `origins:orb_of_origin` inside the 'Id' text box.
3. Click the 'Add' button and drag-and-drop the newly added item that has a black and pink texture into the crafting result slot just beside the crafting grid slots.
4. Create your own pattern.
5. Download as a datapack by clicking on the 'Download datapack.zip' button below.


### Origin (and origin layer) specific Orb

Origins adds an `origins:origin` item component, which makes it possible for items to open the origin selection GUI and enable the player to choose an origin when the said item is used. The Orb of Origin item has this item component defined by default.

To make an item only be able to open the origin selection GUI with select origins or origin layers, you can specify an object (or multiple objects) with an `origin` (optional) and/or `layer` (required) keys in the `origins:origin` item component (which is an array of objects):
```mcfunction
#   Give an Orb of Origin that will automatically select the Avian origin from the `origins:origin` origin layer
give @s origins:orb_of_origin[origins:origin=[{origin: "origins:avian", layer: "origins:origin"}]]


#   Give a stick that will open the origin selection GUI only with the following origin layers: `origins:origin`, `example:hello_world`
give @s minecraft:stick[origins:origin=[{layer: "origins:origin"}, {layer: "example:hello_world"}]]
```

Otherwise, you can specify an empty `origins:origin` item component to have it open all the available and enabled origin layers:
```mcfunction
#   Give an egg that will open the origin selection GUI with all the available and enabled origin layers
give @s minecraft:egg[origins:origin=[]]
```