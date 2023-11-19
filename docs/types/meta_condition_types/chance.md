---
title: Chance (Meta Condition Type)
date: 2023-11-19
---


#	Chance

[Meta Condition Type](../meta_condition_types.md)

Generates a random number between 0.0 and 1.0 and checks if it's less than a specified value.

Type ID: `origins:chance`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`chance` | [Float](../data_types/float.md) | | The value to compare the randomly generated number to.


###	Examples

```json
"condition": {
	"type": "origins:chance",
	"chance": 0.5
}
```

This example will evaluate to true 50% of the time.
