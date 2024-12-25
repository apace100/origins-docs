---
title: Key (Data Type)
date: 2021-04-04
---

# Key

[Data Type](../data_types.md)

An [Object](object.md) which defines a keybinding, used in active powers to define which key they react to.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`key` | [String](string.md) | | A string specifying the keybinding. See [Keybindings](../../misc/extras/keybindings.md) for possible values.
`continuous` | [Boolean](boolean.md) | `false` | Determines how the keybinding behaves when the key is held down. If set to `false`, the power will activate only once when the key is first pressed. If set to `true`, the power will try to activate continuously as long as the key is held down, accounting for any cooldown or conditions the power may have.


### Examples

```json
"key": {
    "key": "key.origins.secondary_active"
}
```

This key will trigger each time the secondary active power key of Origins (by default unbound) is pressed.
<br>

```json
"key": {
    "key": "key.attack",
    "continuous": true
}
```

This key will trigger each tick while the Minecraft attack key (default: left mouse button) is held.