---
title: Add to Set (Bi-entity Action Type)
date: 2023-12-14
---


#	Add to Set

[Bi-entity Action Type](../bientity_action_types.md)

Add the target entity to the power that uses the [Entity Set (Power Type)](../power_types/entity_set.md) of the actor entity.

Type ID: `origins:add_to_set`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`set` | [Identifier](../data_types/identifier.md) | | The ID of the power to add the target entity into.
`time_limit` | [Integer](../data_types/integer.md) | *optional* | If specified, this will determine how long the target entity will be stored in the specified power in ticks.


###	Examples

```json
"bientity_action": {
	"type": "origins:add_to_set",
	"set": "example:entities_to_exclude"
}
```

This example will add the target entity to the `example:entities_to_exclude` (`data/example/powers/entities_to_exclude.json`) power permanently.
<br>

```json
"bientity_action": {
	"type": "origins:add_to_set",
	"set": "example:make_em_glow",
	"time_limit": 200
}
```

This example will add the target entity to the `example:make_em_glow` (`data/example/powers/make_em_glow.json`) power temporarily for 10 seconds, after which the target entity will be removed.
