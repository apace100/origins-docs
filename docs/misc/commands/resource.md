---
title: /resource (Command)
date: 2021-07-13
---

# `/resource`

The `/resource` command can be used to change (add/subtract), get, set, and do operations on resource. Resource operations can only do **scoreboard objective to resource**, not resource to resource.

# Syntax:

```mcfunction
resource has <target> <power>
```

Check if the specified target has a resource power.
<br>

-   `<target>` being a target selector, username, or UUID; can only select one at a time

    -   (e.g: `@a[limit = 1]`, `@p`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

-   `<power>` being the namespace and ID of a power \* (e.g: `test:example_resource` (`data/test/powers/example_resource.json`))
    <br>
    <br>

```mcfunction
resource get <target> <power>
```

Fetch the current value of a (cooldown or resource) power from the specified target.
<br>

-   `<target>` being a target selector, can only select one entity at a time

    -   (e.g: `@a[limit = 1]`, `@p`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

-   `<power>` being the namespace and ID of a power \* (e.g: `test:example_resource` (`data/test/powers/example_resource.json`))
    <br>
    <br>

```mcfunction
resource change <target> <power> <value>
```

Change the value of a specified (cooldown or resource) power of a specified target.
<br>

-   `<target>` being a target selector, can only select one entity at a time

    -   (e.g: `@a[limit = 1]`, `@p`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

-   `<power>` being the namespace and ID of a power

    -   (e.g: `test:example_resource` (`data/test/powers/example_resource.json`))

-   `<value>` being an integer (a whole number)
    <br>
    <br>

```mcfunction
resource operation <target> <power> <operator> <sourceEntity> <sourceObjective>
```

Operate the specified target's resource to a specified source's score in a scoreboard objective.
<br>

-   `<target>` being a target selector, can only select one entity at a time

    -   (e.g: `@a[limit = 1]`, `@p`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

-   `<power>` being the namespace and ID of a power

    -   (e.g: `test:example_resource` (`data/test/powers/example_resource.json`))

-   `<operator>` being an operation

    -   (e.g: `%=`, `*=`, `+=`, `-=`, `/=`, `<`, `=`, `>`, `><`)
    -   `%=` Modulus: Divide target's resource by source's score, and use the remainder to set the target's resource.
    -   `*=` Multiplication: Set the target's resource to the product of the target's and source's operation
    -   `+=` Addition: Add source's score to the target's resource
    -   `-=` Subtraction: Subtract source's score from the target's resource
    -   `/=` Division: Divide target's resource by source's score, and use the result (rounded down) to set the target's resource.
    -   `<` Min: Set the target's resource to the source's score only if source has the lesser score.
    -   `=` Assign: Set the target's resource to the source's score
    -   `>` Max: Set the target's resource to the source's score only if the source has the greater source.
    -   `><` Swap: Swaps the target's resource and the source's score

-   `<sourceEntity>` being a target selector, username, or UUID; can only select one at a time

    -   (e.g: `@a`, `eggohito`, `70ecd8a7-5abb-492a-a3b3-9aae099400db`)

-   `<sourceObjective>` being the scoreboard objective to operate the value of the resource from
    -   (e.g: `testObj` (created with `/scoreboard objectives add testObj dummy`))
