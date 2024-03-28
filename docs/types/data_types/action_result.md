---
title:	Action Result (Data Type)
date:	2021-12-27
alias: test
text: Action Result
---

#	Action Result

[Data Type][data_types]

A [String][string] used to indicate the result of a certain action.


###	Values

Value				|	Description
--------------------|--------------
`consume_partial`	|	Indicates that the action is performed but the actor's hand is not swung and no statistic is incremented.
`consume`			|	Indicates that the action is performed but the actor's hand is not swung.
`fail`				|	Indicates that the action is **not** performed and prevents other actions from performing.
`pass`				|	Indicates that the action is **not** performed but allows other actions to perform.
`success`			|	Indicates that the action is performed and the actor's hand is swung.
