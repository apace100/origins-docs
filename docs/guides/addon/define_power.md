---
title: Defining a Power
date: 2025-01-27
---

# Defining a Power in Java

!!! caution

	This guide is for those who wish to add custom functionality to their powers. If you'd like to make a power using predefined power types, check out [Defining a Power in JSON](../data/define_power/).

Powers are the heart of Origins: they define the functionality that allows each Origin to do cool things. Each Origin is a set of these powers. Behind those powers, however, is a lot of Java code that powers it all!

## Creating a Simple Power with No JSON Data

### Setting up the Power
To create a power, we'll first have to implement the `Power` class. In this tutorial, we'll call it `ExamplePower`. This subclass is typically placed in `<package>.power`, but it doesn't really matter where you put it. You'll then need to create a constructor, like so:

<!-- elaborate on constructor and why -->

```java
public class ExamplePower extends Power {
	public ExamplePower(PowerType<?> type, LivingEntity entity) {
		super(type, entity);
	}
}
```

### Registering the Power
Now we'll need to register the power we just created. In the same directory, make a `factory` directory, then make a `PowerFactories` class. In this tutorial, we'll be calling it `ExamplePowerFactories`.

To register a simple `Power`, we must create a new static void `register()` method. 

```java
public class ExamplePowerFactories {
	public static void register() {

	}
}
```

Within it, we call `PowerFactories.register()` and pass in a call of `Power.createSimpleFactory()`, which accepts a constructor, and an `Identifier`.

If your mod has its own `identifier()` method, go ahead and use that. If you used the [Fabric template mod](https://docs.fabricmc.net/develop/getting-started/creating-a-project), call `Identifier.of()`; where this example puts `example_addon`, use the `MOD_ID` string found in the main entrypoint of your mod. Otherwise, in the first parameter of `Identifier.of()`, put your mod's name, using underscores in place of spaces. In the second parameter, put your `Power`'s name.

As for the constructor, use the lambda reference `ExamplePower::new`, as shown below:

```java
public class ExamplePowerFactories {
	public static void register() {
		PowerFactories.register(() -> Power.createSimpleFactory(ExamplePower::new, Identifier.of("example_addon", "example")))
	}
}
```

Then, in your mod's `onInitialize()` method, call `ExamplePowerFactories.register()`:

```java
public class ExampleMod {
	@Override
	public void onInitialize() {
		ExamplePowerFactories.register();
	}
}

```

<!-- mk power right in init no classes? -->

## Creating a Power with JSON data

### Setting up the Power
To create a power, we'll first have to implement the `Power` class. In this tutorial, we'll call it `ExamplePower`. This subclass is typically placed in `<package>.power`, but it doesn't really matter where you put it. You'll then need to create a constructor. You must pass a `PowerType` and a `LivingEntity` to the superclass, like so:

```java
public class ExamplePower extends Power {
	public ExamplePower(PowerType<?> type, LivingEntity entity) {
		super(type, entity);
	}
}
```

Add the other fields you need after those parameters. You may want to additionally create public accessors for your field.

```java
public class ExamplePower extends Power {
	private String foo;

	public ExamplePower(PowerType<?> type, LivingEntity entity, String foo) {
		super(type, entity);
		this.foo = foo;
	}

	public String getFoo() {
		return foo;
	}
}
```

### Registering the Power
Now we'll need to register the power we just created. In your `Power` class, add a `createFactory()` method. It should be static, and return an object of `PowerFactory` type.

```java
public static PowerFactory createFactory() {

}
```

To return a new `PowerFactory`, we use its constructor. This accepts an `Identifier`, a `SerializableData`, and your `Power`'s constructor.

If your mod has its own `identifier()` method, go ahead and use that. If you used the [Fabric template mod](https://docs.fabricmc.net/develop/getting-started/creating-a-project), call `Identifier.of()`; where this example puts `example_addon`, use the `MOD_ID` string found in the main entrypoint of your mod. Otherwise, in the first parameter of `Identifier.of()`, put your mod's name, using underscores in place of spaces. In the second parameter, put your `Power`'s name.

For your `SerializableData`:

<!-- TODO: explain? -->

```java
public static PowerFactory createFactory() {
	return new PowerFactory<>(Identifier.of("example_addon", "example"),
		new SerializableData()
			.add("foo", SerializableData.STRING, "hello world!"),
		data -> (type, player) -> new ExamplePower(type, player, data.getString("foo"))
		).allowCondition();
	}
}
```

In the same directory as your `Power` class, make a `factory` directory, then make a `PowerFactories` class. In this tutorial, we'll be calling it `ExamplePowerFactories`. Create a new static void `register()` method, call `PowerFactories.register()`, and pass in a reference to your `Power`'s `createFactory` method:

```java
public class ExamplePowerFactories {
	public static void register() {
		PowerFactories.register(ExamplePower::createFactory);
	}
}
```

Then, in your mod's `onInitialize()` method, call `ExamplePowerFactories.register()`:

```java
public class ExampleMod {
	@Override
	public void onInitialize() {
		ExamplePowerFactories.register();
	}
}

```

## Adding functionality into the Power
Whenever you'd like to have something be conditionally available to entities with certain powers, it's very simple. Add `PowerHolderComponent.hasPower()` as a condition, like so:
```java
if (PowerHolderComponent.hasPower(entity, ExamplePower.class)) {
	// Code goes here...
}
```
where `entity` is an object of type `Entity` and `ExamplePower.class` is an class that extends `Power`.
