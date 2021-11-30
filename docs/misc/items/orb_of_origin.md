---
title: Orb of Origin (Items)
date: 2021-11-22
---

# Orb of Origin

[Item](../items.md)

An item that can change the origin(s) of the player upon "use" (right-click).

By default, the Orb of Origins item doesn't have a crafting recipe and lets you pick an origin for every origin layer that's available. You can change either of these things by creating a recipe (JSON file) for the item, and giving the item a custom NBT respectively.

Item ID: `origins:orb_of_origins`

### Creating a custom recipe

You can use [this website](https://crafting.thedestruc7i0n.ca/) to easily create a recipe. To create a recipe for the Orb of Origins item using the website, you can follow these steps:

1. In the 'Ingredients' section on the right side, click on the 'Add Item' button.
2. Enter `Orb of Origin` inside the 'Name' text box and `origins:orb_of_origin` inside the 'Id' text box.
3. Click the 'Add' button and drag-and-drop the newly added item that has a black and pink texture into the crafting result slot just beside the crafting grid slots.
4. Create your own pattern.
5. Download as a datapack by clicking on the 'Download datapack.zip' button below.

### Origin (and origin layer) specific Orb

You can add the `Targets` NBT to the item so that you can only pick a certain origin/from a certain origin layer by using the Orb of Origin.

e.g:
```mcfunction
give @s origins:orb_of_origin{Targets: [{Origin: "origins:avian", Layer: "origins:origin"}]}
```
In this example, this will set your origin to "Avian" if you were to use the given Orb of Origin.