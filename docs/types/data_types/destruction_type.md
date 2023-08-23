---
title:	Destruction Type (Data Type)
date:	2022-04-01
---

#	Destruction Type

[Data Type][data_types]

A [String][string] used to determine the effect of an explosion to the terrain.


###	Values

  Value      |  Description                                                     
-------------|------------------------------------------------------------------
  `break`    |  The explosion will destroy blocks and drop the loot of said blocks.  
  `none`     |  The explosion will **not** destroy blocks nor drop the loot of said blocks.  
  `destroy`  |  The explosion will destroy blocks and drop the loot of *some* of the said blocks. It has lower chance with higher explosion power; it also checks the `minecraft:survives_explosion` loot condition in loot tables.  
