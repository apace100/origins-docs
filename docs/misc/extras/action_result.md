---
title: Action Result (Extras)
date: 2021-12-27
---

#   Action Result
Action Results are [String](../../types/data_types/string.md) enumerated type used for determining the result of an action.


### List

Action Result | Description
--------------|------------
`"consume"` | Indicates that the action is performed but the actor's hand is not swung.
`"consume_partial"` | Indicates that the action is performed but the actor's hand is not swung and no statistic is incremented.
`"fail"` | Indicates that the action is **not** performed and prevents other actions from being performed.
`"pass"` | Indicates that the action is **not** performed but allows other actions to be done.
`"success"` | Indicates that the action is performed and the actor's hand is swung.
