---
title: Defining a Power Type
date: 2025-01-06
---

# Defining a Power Type in Java
**Important:** This guide is for those who wish to add custom functionality to their powers. If you'd like to make a power using predefined power types, check out [Defining a Power in JSON](../data/define_power/).

Powers are the heart of Origins: they define the functionality that allows each Origin to do cool things. Each Origin is a set of these powers. Behind those powers, however, are **power types**: this is the code behind each power.

## Tutorial

### Setting up the PowerType
To create a power type, we'll first have to implement the abstract `PowerType` class. In this tutorial, we'll call it `ExamplePowerType`. This subclass is typically placed in `<package>.power.type`, but it doesn't really matter where you put it. You'll then need to create a constructor, which you can simply leave blank for now, like so:

```java
public class ExamplePowerType extends PowerType {
	public ExamplePowerType() {

	}
}
```

### Registering the PowerType
Now we'll need to register the power type we just created. In the same directory, make a `PowerTypes` class. In this tutorial, we'll be calling it `ExamplePowerTypes`.

To register a `PowerType`, we need to write our own method. This is relatively simple; we must cast from a `PowerConfiguration<PowerType>` to a `PowerConfiguration<ExamplePowerType>`, and the Apoli API handles the rest. You may simply copy the code below:

```java
public class ExamplePowerTypes {
	public static <T extends PowerType> PowerConfiguration<T> register(PowerConfiguration<T> configuration) {
		PowerConfiguration<PowerType> casted = (PowerConfiguration<PowerType>) configuration;
		Registry.register(ApoliRegistries.POWER_TYPE, casted.id(), casted);
		return configuration;
	}
}
```
You may want to additionally suppress the unchecked cast warning.

Now, to use the method, we pass into `register()` a call of `PowerConfiguration.dataFactory()`. This method wants an `Identifier`, and a constructor.

If your mod has its own `identifier()` method, go ahead and use that. If you used the [Fabric template mod](https://docs.fabricmc.net/develop/getting-started/creating-a-project), call `Identifier.of()`; where this example puts `example_addon`, use the `MOD_ID` string found in the main entrypoint of your mod. Otherwise, in the first parameter of `Identifier.of()`, put your mod's name, using underscores in place of spaces.

As for the constructor, use a lambda reference, as shown below:

```java
public static final PowerConfiguration<ExamplePowerType> EXAMPLE_POWER_TYPE = register(
	PowerConfiguration.dataFactory(Identifier.of("example_addon", "example_power_type"), ExamplePowerType::new)
);
```
In cases where the name of your power is a bit more verbose, you may omit `_POWER_TYPE`—for example, in the case of a `BouncinessPowerType`, the registered variable may be simply called `BOUNCINESS`.

The last step is to make a static void method `register()`. There doesn't need to be any code inside it:
```java
public static void register() {

}
```

And in the main entrypoint of your mod, call it within `onInitialize()`, like so:
```java
public void onInitialize() {
	ExamplePowerTypes.register();
}
```

You may have noticed that in the previous section, there was one abstract method `getConfig()` that we didn't override. Navigate back to your `ExamplePowerType` class, and within it place this code, referencing the variable containing your registered `PowerType`:

```java
@Override
public @NotNull PowerConfiguration<?> getConfig() {
	return ExamplePowerTypes.EXAMPLE_POWER_TYPE;
}
```

### Adding functionality into the PowerType
Whenever you'd like to link functionality to a power type, there's only one step to it. Wrap everything in an `if` statement, and add `PowerHolderComponent.hasPowerType()` as a condition, like so:
```java
if (PowerHolderComponent.hasPowerType(entity, ExamplePowerType.class)) {
	// Code goes here...
}
```
where `entity` is an object of type `Entity` and `ExamplePowerType.class` is an class that extends `PowerType`.