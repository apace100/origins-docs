---
title: Damage Source (Data Type)
date: 2021-04-04
---

# Damage Source

[Data Type](../data_types.md)

An [Object](object.md) used to specify how to deal damage to an entity.


!!! danger

	This data type has been <span style="color:darkred"><b>deprecated</b></span> since Minecraft 1.19.4 in favor of using damage types and damage type tags. Associated fields may be removed in a future version. [See here for a more detailed information](https://gist.github.com/apace100/bfbf82a8f9d6bd2db13e4feaf653a6b0)

	See [Minecraft Wiki: Damage type](https://minecraft.wiki/w/Damage_type) and [Minecraft Wiki: Tags (Damage types)](https://minecraft.wiki/w/Tag#Damage_types) for more information about vanilla damage types and damage type tags.


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