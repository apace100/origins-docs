---
title: Float (Data Type)
date: 2021-04-03
---
# Float

[Data Type](../data_types.md).

A floating point (decimal) number, like `6.0`, `-1.5` or `0.1`.

### Example:

```json
{
	"condition": {
		"type": "origins:relative_health",
		"comparison": "<=",
		"compare_to": 0.5
	}
}
```

An [`origins:relative_health` entity condition](../entity_conditions/relative_health.md) that has a `compare_to` float value of `0.5`.