---
title: Undirected (Bi-entity Condition)
date: 2021-10-12
---
# Undirected

[Bi-entity Condition](../bientity_conditions.md)

Checks if the specified bi-entity condition is true before or after swapping the actor and target context.

Type ID: `origins:undirected`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`condition` | [Bi-entity Condition](../bientity_conditions.md) | | The bi-entity condition to check for.

### Examples
```json
"bientity_condition": {
	"type": "origins:undirected",
	"condition": {
		"type": "origins:owner"
	}
}
```
This example will return true if the actor entity is the owner of the target entity, or if the target entity is the owner of the actor entity.