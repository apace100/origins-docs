---
title: Grant Advancement (Entity Action Type)
date: 2023-05-23
---

# Grant Advancement

[Entity Action Type](../entity_action_types.md)

Grants an advancement to the player.

Type ID: `origins:grant_advancement`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`advancement` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the advancement to be granted to the player.
`criteria` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | _optional_ | If specified, determines the criteria to grant to the specified advancement.
`criterion` | [String](../data_types/string.md) | _optional_ | If specified, determines the criterion to grant to the specified advancement.
`selection` | [String](../data_types/string.md) | `"only"` | Determines how to select the parent advancement(s) or child(ren) advancement(s) of the specified advancement. Can be one of: `"only"`, `"through"`, `"from"`, `"until"`, `"everything"`

### Examples

```json
"entity_action": {
    "type": "origins:grant_advancement",
    "advancement": "minecraft:adventure/arbalistic"
}
```

This example will grant the player the Arbalistic advancement.
