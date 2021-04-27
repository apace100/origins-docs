---
title: Elytra Flight (Power Type)
date: 2021-04-07
---
# Elytra Flight

[Power Type](../power_types.md).

Allows the player to fly as if they had an Elytra equipped.

Type ID: `origins:elytra_flight`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`render_elytra` | [Boolean](../data_types/boolean.md) |  | Whether an Elytra should render on the player's back while this power is active.


### Example
```json
{
    "type": "origins:elytra_flight",
    "render_elytra": false
}
```
This power gives the player the ability to fall-fly, with the elytra not being rendered.