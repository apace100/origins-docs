---
title: /power (Command)
date: 2021-06-13
---

# `/power`

The `/power` command can be used to grant powers, revoke powers, and check if an entity has a certain power. Powers can only be granted once by one source.
<br>
<br>

```mcfuncton
power clear <selector>
```
* `<selector>` being a target selector.
    * (e.g: `@a[tag = tagName]`)
<br>


```mcfunction
power grant <selector> <power> [<source>]
```
* `<selector>` being a target selector
    * (e.g: `@a[tag = tagName]`)

* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin`)

* `[<source>]` being the source of the power, optional, defaults to `apoli:command`
    * (e.g: `example:test`)
<br>

```mcfunction
power has <selector> <power>
```
* `<selector>` being a target selector.
    * (e.g: `@a[tag = tagName]`)

* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin`)
<br>

```mcfunction
power list @s
```
* `<selector>` being a target selector, can only select one at a time.
    * (e.g: `@a[limit = 1, sort = random]`)
<br>

```mcfunction
power remove <selector> <power>
```
* `<selector>` being a target entity selector.
    * (e.g: `@a[tag = tagName]`)

* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin`)
<br>

```mcfunction
power revoke <selector> <power> [<source>]
```
* `<selector>` being a target selector.
    * (e.g: `@a[tag = tagName]`)

* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin`)

* `[<source>]` being the source of the power, defaults to `apoli:command`.
    * (e.g: `example:test`)
<br>

```mcfunction
power revokeall <selector>
```
* `<selector>` being a target selector.
    * (e.g: `@a[tag = tagName]`)
<br>

```mcfunction
power sources @s origins:creative_flight
```
* `<selector>` being a target selector, can only select one at a time.
    * (e.g: `@a[limit = 1, sort = random]`)

* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin`)