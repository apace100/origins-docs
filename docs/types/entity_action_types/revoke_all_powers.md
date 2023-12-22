---
title: Revoke All Powers (Entity Action Type)
date: 2023-10-26
---


#	Revoke All Powers

[Entity Action Type](../entity_action_types.md)

Revoke all powers from the specified source.

Type ID: `origins:revoke_all_powers`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`source` | [Identifier](../data_types/identifier.md) | | The ID of the source to revoke powers from.


###	Examples

```json
"entity_action": {
	"type": "origins:revoke_all_powers",
	"source": "origins:blazeborn"
}
```

This example will revoke all powers granted by the Blazeborn origin.
