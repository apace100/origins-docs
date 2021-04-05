---
title: Space
date: 2021-04-05
---

# Space

A space is a string which defines which coordinate system is used for directions, currently it's only used in [Add Velocity](../entity_actions/add_velocity.md). This means a space defines what "y" and "z" mean.

* `world`: The axes are global, "y" is always the up-down axis.
* `local`: The axes are recalculated such that "z" is always the direction the entity is facing. Keep in mind that there are several orientations in which this is the case, thus "y" and "x" might not behave the way you'd expect.
* `velocity`: The axes are recalculated such that "z" points towards the direction of the current velocity of the entity. They are also scaled to match the velocity.
* `velocity_normalized`: Same as `velocity`, however the axes are normalized.
* `velocity_horizontal`: Same as `velocity`, however the upwards velocity is set to 0.
* `velocity_horizontal_normalized`: Same as `velocity_horizontal`, however the axes are normalized.
