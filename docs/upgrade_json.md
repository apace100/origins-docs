---
title: Upgrade JSON
date: 2021-04-05
---
# Upgrade JSON Format

An [Object](data_types/object.md) used to specify an upgrade of an origin within an [Origin JSON](origin_json.md).


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Identifier](data_types/identifier.md) | | ID of an advancement which should trigger this upgrade.
`origin` | [Identifier](data_types/identifier.md) | | ID of an origin the origin with this upgrade should upgrade to.
`announcement` | [String](data_types/string.md) | _optional_ | A text which will show up in the local chat of the player in a pretty color. If none is specified, there won't be a message.
