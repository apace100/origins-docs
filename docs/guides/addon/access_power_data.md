---
title: Accessing Power Data
date: 2025-01-27
---

# Accessing Power Data

There are several ways to read data defined in Power JSONs. 

## If players have only one of each `PowerType`
Assuming that a player would only have one instance of any `PowerType`, we can write this method:
```java
public static <T extends PowerType> T getPowerInstance(Entity entity, Class<T> powerType) throws IndexOutOfBoundsException {
	List<T> powerList = PowerHolderComponent.getPowerTypes(entity, powerType);
	return powerList.getFirst();
}
```
This method would retrieve all the Powers of an entity matching the specified `PowerType`, and return the first in the `List`. If it's not found, however, it will throw `IndexOutOfBoundsException`, which should be caught with enough grace to prevent the game from crashing.

Alternatively, we can use streams to ensure null safety:
```java
public static <T extends PowerType> Optional<T> getPowerInstance(Entity entity, Class<T> powerType) throws NoSuchElementException {
	return PowerHolderComponent.getPowerTypes(entity, powerType).stream().findFirst();
}
```
This returns the instance of the `PowerType` wrapped in an `Optional`. To access the `PowerType`, use `getPowerInstance(entity, powerType).orElseThrow()`. Be careful, though—a value not found will throw `NoSuchElementException`. You can use `isPresent()` to check whether the `Optional` holds a value.

`orElseThrow()` also has an overload allowing you to throw your own `Exception` by passing it into the method, if you'd like.