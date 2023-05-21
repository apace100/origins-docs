---
title: Damage Source (Data Type)
date: 2021-04-04
---

# Damage Source

[Data Type](../data_types.md)

An [Object](object.md) used to specify how to deal damage to an entity.

!!! danger

    The concept of damage sources is deprecated. Associated fields may be removed in a future version. Any power or action requiring you to specify a damage source, will now have a way to specify a damage type instead (usually a field called `damage_type`) which should be used instead. [More information here](https://gist.github.com/apace100/bfbf82a8f9d6bd2db13e4feaf653a6b0).



### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`name` | [String](string.md) | | The name of the damage source. Controls death message as well as other interactions. Consider the [List of Damage Source Names](../../misc/extras/damage_source_names.md) when picking a name.
`bypasses_armor` | [Boolean](boolean.md) | `false` | When true, armor values are not taken into account when calculating the actual damage amount taken.
`fire` | [Boolean](boolean.md) | `false` | When true, the damage will be considered fire damage.
`unblockable` | [Boolean](boolean.md) | `false` | When true, the damage will be unblockable (not reduced by resistance effects or protection enchantments).
`magic` | [Boolean](boolean.md) | `false` | When true, the damage will be considered magic damage.
`out_of_world` | [Boolean](boolean.md) | `false` | When true, the damage will be considered "out of world" damage, i.e. damage from falling into the void.


### Examples

```json
"source": {
	"name": "starve",
	"bypasses_armor": true,
	"unblockable": true
}
```

A damage source which specifies damage similar to the one caused by starvation.