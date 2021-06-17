---
title: /resource (Command)
date: 2021-06-13
---

# `/resource`

The `/resource` command can be used to change (add/subtract), get, set, and do operations on resource. Resource operations can only do __scoreboard objective to resource__, not resource to resource.
<br>
<br>

```mcfunction
resource has <target> <power>
```
* `<target>` being a target selector, can only select one entity at a time.
    * (e.g: `@a[limit = 1, sort = random]`)

* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))
<br>

```mcfunction
resource get <target> <power>
```
* `<target>` being a target selector, can only select one entity at a time.
    * (e.g: `@a[limit = 1, sort = random]`)

* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))
<br>

```mcfunction
resource change <target> <power> <value>
```
* `<target>` being a target selector, can only select one entity at a time.
    * (e.g: `@a[limit = 1, sort = random]`)

* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))

* `<value>` being an integer.
<br>

```mcfunction
resource operation <target> <power> <operation> <sourceEntity> <sourceObjective>
```
* `<target>` being a target selector, can only select one entity at a time.
    * (e.g: `@a[limit = 1, sort = random]`)

* `<power>` being the namespace and ID of a power.
    * (e.g: `origins:arcane_skin` (`data/origins/powers/arcane_skin.json`))

* `<operation>` being an operation.
    * (e.g: `%=`, `*=`, `+=`, `-=`, `/=`, `<`, `=`, `>`, `><`)

* `<sourceEntity>` being a target selector, to select the entity to operate the score from, can only select one at a time.
    * (e.g: `@a[tag = tagName]`)

* `<sourceObjective>` being the scoreboard objective to operate the value of the resource from.
    * (e.g: `testObj` (created with `/scoreboard objectives add testObj dummy`))