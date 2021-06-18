---
title: /origin (Command)
date: 2021-06-12
---

# `/origin`

The `/origin` command can be used to check for origins/powers, and set the player's origin from a specified origin layer.
<br>
<br>

```mcfunction
origin get <selector> <originLayer>
```
* `<selector>` being a target selector, can only select one at a time.
    * (e.g: `@a[limit = 1]`)
* `<originLayer>` being the namespace and ID of an origin layer.
    * (e.g: `origins:origin`)
<br>

```mcfunction
origin has origin <selector> <originLayer> <origin>
```
* `<selector>` being a target selector.
    * (e.g: `@a[tag = tagName]`)
* `<originLayer>` being the namespace and ID of an origin layer.
    * (e.g: `origins:origin`)
* `<origin>` being the namespace and ID of an origin.
    * (e.g: `origins:human`)
<br>

```mcfunction
origin has power <selector> <power>
```
* `<selector>` being a target selector.
    * (e.g: `@a[tag = tagName]`)
* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin`)
<br>

```mcfunction
origin set <selector> <originLayer> <origin>
```
* `<selector>` being a target selector.
    * (e.g: `@a[tag = tagName]`)
* `<originLayer>` being the namespace and ID of an origin layer.
    * (e.g: `origins:origin`)
* `<origin>` being the namespace and ID of an origin.
    * (e.g: `origins:human`)