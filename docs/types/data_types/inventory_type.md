---
title:	Inventory Type (Data Type)
date:	2022-06-15
---

#	Inventory Type

[Data Type][data_types]

A [String][string] used to determine whether to reference the inventory of the entity or the inventory of a power present in the entity.

!!!	note

	Not to be confused with the [Container Type (Data Type)][container_type]


###	Values

  Value        |  Description                                                   
---------------|----------------------------------------------------------------
  `inventory`  |  Determines that the inventory of the entity will be referenced, if they have one.  
  `power`      |  Determines that the inventory of a power will be referenced. (e.g: a power that uses the [Inventory (Power Type)](../power_types/inventory.md))  
