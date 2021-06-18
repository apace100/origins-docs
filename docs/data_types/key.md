---
title: Key (Data Type)
date: 2021-04-04
---
# Key

[Data Type](../data_types.md).

An [Object](object.md) which defines a keybinding, used in active powers to define which key they react to.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`key` | [String](string.md) | | A string specifying the keybinding. See [Keybindings](../misc/keybindings.md) for possible values.
`continuous` | [Boolean](boolean.md) | false | Whether the keybinding should only trigger the power on the first tick the key is held down, or, if set to true, continuously on each tick while the key is held.

### Examples:

```json
{
  	"key": {
		"key": "key.origins.secondary_active"
  	}
}
```

This key will trigger each time the secondary active power key of Origins (by default unbound) is pressed.
<br>

```json
{
  	"key": {
		"key": "key.attack",
		"continuous": true
  	}
}
```

This key will trigger each tick while the Minecraft attack key (default: left mouse button) is held.