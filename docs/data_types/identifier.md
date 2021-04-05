---
title: Identifier (Data Type)
date: 2021-04-04
---
# Identifier

[Data Type](../data_types.md).

A [String](string.md) which specifies an identifier used in Minecraft. They are used to refer to items, blocks, status effects, locations in data or resource packs, and a lot of other things.


An identifier consists of a namespace and a path. Namespace and path are separated with a colon. An identifier may only contain lower-case letters (a-z), digits (0-9), `-`, `_` and `.`. It can include at most a single colon (`:`) for separation. The path may contain `/` to indicate "folders", but the namespace may not.

If no namespace is specified, it will default to `minecraft`.

Read more here: https://minecraft.fandom.com/wiki/Namespaced_ID

### Example

```json
{
	"field_name": "iron_ore"
}
```
An identifier specifying iron ore. The namespace is not specified, thus defaults to `minecraft`.

```json
{
	"field_name": "origins-classes:stealth"
}
```
An identifier specifying the stealth status effect added by the Origins: Classes add-on.
