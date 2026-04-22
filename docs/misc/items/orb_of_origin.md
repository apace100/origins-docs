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

Origins adds an [`origins:origin` item component](../../misc/component_types/origin.md), which makes it possible for items to open the origin selection GUI and enable the player to choose an origin when the said item is used. The Orb of Origin item has this item component defined by default.

Here are some examples of how it can be used:
<ul>

<li>

```mcfunction
give @s minecraft:stick[origins:origin = []]
```
This example will define an <code>origins:origin</code> component to a Stick item that enables the player to select from all the available and enabled origin layers when the item is used.

</li>
<br>

<li>

```mcfunction
give @s origins:orb_of_origin[origins:origin = [{layer: "origins:origin"}, {layer: "example:hello_world"}]]
```
This example will define an <code>origins:origin</code> component to an Orb of Origins item that enables the player to only select an origin from the defined origin layers (<code>origins:origin</code> and <code>example:hello_world</code>) when the item is used.

</li>
<br>

<li>

```mcfunction
give @s minecraft:egg[origins:origin = [{layer: "origins:origin", origin: "origins:arachnid"}]]
```
This example will define an <code>origins:origin</code> component to an Egg item that will automatically set the origin of the player in the <code>origins:origin</code> origin layer to <code>origins:arachnid</code> origin.

</li>

</ul>
