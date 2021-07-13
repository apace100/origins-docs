---
title: /power (Command)
date: 2021-07-13
---

# `/power`

The `/power` command can be used to grant powers, revoke powers, and check if an entity has a certain power. There can only be one power per power source.

### Syntax:

```mcfunction
power clear <targets>
```
Clear all the powers from the specified target(s).
<br>

* `<targets>` being a target selector, username, or UUID
    * (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)
<br>
<br>

```mcfunction
power grant <targets> <power> [<source>]
```
Grant a power to the specified target(s) (from a specific power source, if specified)
<br>

* `<targets>` being a target selector, username, or UUID
    * (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

* `<power>` being the namespace and ID of a power
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))

* `[<source>]` being the source of the power; optional; defaults to `apoli:command`
    * (e.g: `example:test`)
<br>
<br>

```mcfunction
power has <targets> <power>
```
Check if the specified target(s) has a certain power.
<br>

* `<targets>` being a target selector, username, or UUID
    * (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

* `<power>` being the namespace and ID of a power
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))
<br>
<br>

```mcfunction
power list <target>
```
List all the powers available from the specified target.
<br>

* `<target>` being a target selector, username, or UUID; can only select one at a time.
    * (e.g: `@a[limit = 1]`, `@p`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)
<br>
<br>

```mcfunction
power remove <targets> <power>
```
Remove a power from the specified target.
<br>

* `<targets>` being a target selector, username, or UUID
    * (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

* `<power>` being the namespace and ID of a power
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))
<br>
<br>

```mcfunction
power revoke <targets> <power> [<source>]
```
Revoke a power from the specified target(s) (and from a specific power source, if specified.)
<br>

* `<targets>` being a target selector, username, or UUID
    * (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

* `<power>` being the namespace and ID of a power
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))

* `[<source>]` being the source of the power, defaults to `apoli:command`
    * (e.g: `example:test`)
<br>
<br>

```mcfunction
power revokeall <targets>
```
Revoke all the powers from the specified target(s).
<br>

* `<targets>` being a target selector, username, or UUID
    * (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)
<br>
<br>

```mcfunction
power sources <target> <power>
```
List all the sources of a power from the specified target.
<br>

* `<target>` being a target selector, username, or UUID; can only select one at a time
    * (e.g: `@a[limit = 1]`, `@p`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

* `<power>` being the namespace and ID of a power
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))