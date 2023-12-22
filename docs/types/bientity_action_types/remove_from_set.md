---
title: Remove from Set (Bi-entity Action Type)
date: 2023-12-14
---


#	Remove from Set

[Bi-entity Action Type](../bientity_action_types.md)

Removes the target entity from the power that uses the [Entity Set (Power Type)](../power_types.md) of the actor entity.

Type ID: `origins:remove_from_set`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`set` | [Identifier](../data_types/identifier.md) | | The ID of the power to remove the target entity from.


###	Examples

```json
"bientity_action": {
	"type": "origins:remove_from_set",
	"set": "example:entities_to_exclude"
}
```

This example will remove the target entity from the `example:entities_to_exclude` (`data/example/powers/entities_to_exclude.json`) power.
