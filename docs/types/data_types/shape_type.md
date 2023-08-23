---
title:	Shape Type (Data Type)
date:	2021-01-04
---

#	Shape Type

[Data Type][data_types]

A [String][string] used to determine how raycasts will handle blocks.


###	Values

  Value       |  Description                                                    
--------------|-----------------------------------------------------------------
  `collider`  |  The ray will only stop at blocks with collision. *(e.g: blocks that cannot be walked through)*  
  `outline`   |  The ray will take the shape of the block into account, only stopping if the ray has hit a face of a block.  
  `visual`    |  The ray will only stop at blocks that are not considered transparent. *(e.g: blocks that aren't see-through)*  
