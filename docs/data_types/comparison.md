---
title: Comparison (Data Type)
date: 2021-04-04
---
# Comparison

[Data Type](../data_types.md).

A [String](string.md) which specifies how two numbers should be compared. Usually the first number is provided by whatever condition you are in, and the second is specified in an accompanying `compare_to` field.

### Values

Value  | Description
-------|------
`<` | Checks if the first number is **less than** the second number.
`<=` | Checks if the first number is **less than or equal to** the second number.
`>` | Checks if the first number is **greater than** the second number.
`>=` | Checks if the first number is **greater than or equal to** the second number.
`==` | Checks if the first number is **equal to** the second number.
`!=` | Checks if the first number is **not equal to** the second number.

### Examples

```json
{
	"comparison": "=="
}
```

Equal to. There's not much to say about this.
<br>

```json
{
	"condition": {
		"type": "origins:xp_levels",
		"comparison": ">=",
		"compare_to": 3
	}
}
```

A comparison used inside an [XP Levels](../entity_conditions/xp_levels.md) condition, which checks that the player is level 3 or higher.