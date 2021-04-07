---
title: Multiple (Power Type)
date: 2021-04-07
---
# Multiple

[Power Type](../power_types.md).

Allows defining more than one power in a single file. The "sub-powers" are hidden by default. When the "super-power" (the file this `origins:multiple` is in) is added to an origin, all sub-powers are added automatically.

Type ID: `origins:multiple`

### Fields

Arbitrary fields. Any "key" is considered a sub-power, and takes a fully-defined power type as the value. You can reference sub-powers by using the super-power ID, appended by an underscore (`_`) and lastly the sub-power ID (which is the key), i.e. `<namespace>:<powerfile>_<subpower>`

### Example: [Master of Webs](https://github.com/apace100/origins-fabric/blob/master/src/main/resources/data/origins/powers/master_of_webs.json)
