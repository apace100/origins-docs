---
title: Identifier (Data Type)
date: 2021-04-04
---

# Identifier

[Data Type](../data_types.md)

A [String](string.md) which specifies an identifier used in Minecraft. They are used to refer to items, blocks, status effects, locations in data or resource packs, and a lot of other things.

An identifier consists of a namespace and a path. Namespace and path are separated with a colon. An identifier may only contain lower-case letters (a-z), digits (0-9), `-`, `_` and `.`. It can include at most a single colon (`:`) for separation. The path may contain `/` to indicate "folders", but the namespace may not.

If no namespace is specified, it will default to `minecraft`.

Read more here: [Minecraft Fandom Wiki: Namespaced ID](https://minecraft.fandom.com/wiki/Namespaced_ID)

### Examples

```json
{
	"type": "apoli:block",
	"block": "iron_ore"
}
```

A `block` identifier specifying iron ore. The namespace is not specified, thus defaults to `minecraft`.
<br>

```json
{
	"type": "apoli:power",
	"power": "test:example_power"
}
```

A `power` identifier specifying the `test:example_power` power (located on `data/test/powers/example_power.json`).
