---
title: Dependencies
date: 2021-07-17
---
# Explaining Origins' dependencies

You probably noticed there was a huge chunk of repositories you had to add in the previous step in order to include Origins in your project. That's because Origins itself depends on many other libraries:

Library | Responsibility | Used By
--------|----------------|---------
[Apoli](https://github.com/apace100/apoli) | data-driven powers | Origins
[Calio](https://github.com/apace100/calio) | serialization of data | Origins, Apoli
[FallFlyingLib](https://github.com/CafeteriaGuild/FallFlyingLib) | compatibility of Elytra flight mods | Apoli
[PlayerAbilityLib](https://github.com/Ladysnake/PlayerAbilityLib) | compatibility of mods which modify "abilities" (such as creative flight) | FallFlyingLib, Apoli
[Cardinal Components API](https://github.com/OnyxStudios/Cardinal-Components-API) | attaching data to objects | Origins, Apoli
[Cloth Config](https://github.com/shedaniel/cloth-config) | easy creation of configuration files and screens | Origins
([Mod Menu](https://github.com/TerraformersMC/ModMenu)) | showing mods, allowing modders to add configuration in-game | Origins

Origins bundles all of these (except Mod Menu, which is an optional dependency) in the final JAR that players download, in order to make the life of players who install the mod easier.

The most important libraries of which you'll need to understand their functionality and distinction are going to be Apoli and Calio. Their features were originally a part of Origins, but were extracted so I (and other developers too, of course) could use them for other mods!

### Calio

Origins is very focused on reading and handling JSON data, as well as sending that data across the network to players (to make datapacks be only required on the server-side). Usually, you'd have to check the existence of JSON fields manually, read them in specifically for the object you want to construct, and then also create a `read` and `write` method which sends and receives data from `PacketByteBuf`s.

Having to do this several times for each new object you want to read means the code will be very error-prone, you'd have a lot of redundancy because you'd write error handling code more often than once, and might cause inconsistencies in error handling if you're not careful.

That's where the `SerializableData` system added by Calio comes in. It allows defining a group of JSON fields you want to read from a file, along with their corresponding data types. You can specify optional fields, and fields with default values if you want. The system also has easy-to-use methods for sending and receiving data across the network.
Error handling is defined per type. Each data type that a field can assume is defined as a `SerializableDataType`, with its own `read`, `write`, and `receive` methods. Most of the usual data types in Java and vanilla Minecraft are defined statically in the `SerializableDataTypes` class.

### Apoli

Apoli actually contains the bulk of logic for the Origins mod. It contains the power system, allowing to assign powers to players, as well as conditions and actions. It handles reading these from JSON (via Calio's system), and by itself allows attaching powers to entities with the `power` command, or when used as a library from code. Powers can be added to entities from different sources, so for example adding an amulet that grants a power won't conflict with an origin which grants the same power.

After the split of Origins into the three mods (Calio, Apoli and Origins), Origins as a mod boiled down to depending on Apoli as a library, and just adding the "origins system" as a way to let players choose a set of powers at the start of the game.

Almost all of the conditions, actions and power types which are documented on this wiki are part of Apoli. Origins adds (or overrides) a few of these, as they interact with Origins directly: the `origin` condition and `action_on_callback` power type.

Apart from that, Origins defines some specific power functionality which aren't generalized to a power type yet. See [Handling unique powers](unique_powers.md) for more information on how this is done.

Most of what you'll do in an Origins add-on will interact with Apoli directly, and not Origins. Some developers even decided to not make an "Origins add-on" per se, but instead create their own Apoli add-on in which they added the power types they needed, and then built their Origin add-ons on top of that. How you structure your mod in the end is up to you.
