---
title: /origin (Command)
date: 2021-07-13
---

# `/origin`

The `/origin` command can be used to check for origins/powers, and set the player's origin from a specified origin layer.

### Syntax:

```mcfunction
origin get <target> <originLayer>
```
Fetch the origin of the specified target from a specified origin layer.
<br>

* `<target>` being a target selector, username, or UUID; can only select one at a time
    * (e.g: `@a[limit = 1]`, `@p`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)
* `<originLayer>` being the namespace and ID of an origin layer
    * (e.g: `origins:origin` (`data/origins/origin_layers/origin.json`))
<br>
<br>

```mcfunction
origin has origin <targets> <originLayer> <origin>
```
Check if the specified target(s) has a specified origin from a specified origin layer.
<br>

* `<targets>` being a target selector, username, or UUID
    * (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)
* `<originLayer>` being the namespace and ID of an origin layer
    * (e.g: `origins:origin` (`data/origins/origin_layers/origin.json`))
* `<origin>` being the namespace and ID of an origin
    * (e.g: `origins:human` (`data/origins/origins/human.json`))
<br>
<br>

```mcfunction
origin has power <targets> <power>
```
Check if the specified target(s) has the specified power.
<br>

* `<targets>` being a target selector, username, or UUID
    * (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)
* `<power>` being the namespace and ID of a power
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))
<br>
<br>

```mcfunction
origin set <targets> <originLayer> <origin>
```
Set the specified target(s) origin in a specified origin layer.
<br>

* `<targets>` being a target selector, username, or UUID
    * (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)
* `<originLayer>` being the namespace and ID of an origin layer
    * (e.g: `origins:origin` (`data/origins/origin_layers/origin.json`))
* `<origin>` being the namespace and ID of an origin
    * (e.g: `origins:human` (`data/origins/origins/human.json`))