---
title: Action Result (Extras)
date: 2021-12-27
---

#   Action Result
Action Results are [Strings](../../types/data_types/string.md) used for determining the result of an action.


### List

Action Result | Description
--------------|------------
`"consume"` | Indicates that the action is performed but the actor's hand is not swung.
`"consume_partial"` | Indicates that the action is performed but the actor's hand is not swung and no statistic is incremented.
`"fail"` | Indicates that the action is **not** performed and prevents other actions from performing.
`"pass"` | Indicates that the action is **not** performed but allows other actions from performing.
`"success"` | Indicates that the action is performed and the actor's hand is swung.
