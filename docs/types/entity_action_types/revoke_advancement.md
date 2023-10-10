---
title: Revoke Advancement (Entity Action Type)
date: 2023-05-21
---

# Revoke Advancement

[Entity Action Type](../entity_action_types.md)

Revokes an advancement from the player.

Type ID: `origins:revoke_advancement`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`advancement` | [Identifier](../data_types/identifier.md) | _optional_ | The namespace and ID of the advancement to be revoked from the player.
`criteria` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | _optional_ | If specified, determines the criteria to revoke from the specified advancement.
`criterion` | [String](../data_types/string.md) | _optional_ | If specified, determines the criterion to revoke from the specified advancement.
`selection` | [String](../data_types/string.md) | _optional_ | Determines how to select the parent advancement(s) or child(ren) advancement(s) of the specified advancement. Can be one of: `"only"`, `"through"`, `"from"`, `"until"`, `"everything"`



### Examples

```json
"entity_action": {
    "type": "origins:revoke_advancement",
    "advancement": "minecraft:adventure/arbalistic"
}
```

This example will revoke the Arbalistic advancement from the player, if they have it.
