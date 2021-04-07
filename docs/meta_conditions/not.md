---
title: Not / Invert (Condition)
date: 2021-04-07
---
# Not / Invert

[Meta Condition](../meta_conditions.md).

**There is no** meta condition to invert the results of another condition. However, **every** condition supports the following field, which can be used to achieve the same:

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`inverted` | [Boolean](../data_types/boolean.md) | false | If true, the condition acts inverted.

### Example

```json
"condition": {
  "type": "origins:sprinting",
  "inverted": true
}
```
This condition added to a power means the power will only be active when the player is _not_ sprinting.
