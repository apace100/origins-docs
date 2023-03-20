---
title: Layer (JSON Format)
date: 2021-04-05
---

# Layer JSON Format

This is the format of a JSON file describing an origin layer. Origin layers are a collection of origins used for making a player choose one origin for each existing origin layer. For example, the classes from the **Origins: Classes** add-on are on a separate layer, thus you can choose a "class" *in addition to* choosing an origin.

Origin Layer JSON files need to be placed inside the `data/<namespace>/origin_layers` folder of your datapack. The said files can be referenced as `namespace:path/to/origin_layer` (`data/namespace/origin_layers/path/to/origin_layer`) in the [`/origin` (Command)](../misc/commands/origin.md).

The most common use is to create a file with the name `origin.json` in the `data/origins/origin_layers` folder of your datapack with a `replace` Boolean field value of `false`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`order` | [Integer](../types/data_types/integer.md) | _optional_ | Specifies the order of this layer in the choose and view origin screen among the other layers. Smaller numbers mean it appears before layers with larger numbers.
`origins` | [Array](../types/data_types/array.md) of [Identifiers](../types/data_types/identifier.md) and/or [Conditioned Origins](conditioned_origin.md) | | Defines the origins that should be in this layer. [Identifier](../types/data_types/identifier.md) strings and [Conditioned Origin](conditioned_origin.md) objects can be mixed in the same array.
`enabled` | [Boolean](../types/data_types/boolean.md) | `true` | If set to false, this layer will be unavailable.
`replace` | [Boolean](../types/data_types/boolean.md) | `false` | If set to false, the data in this file will be appended to an already existing version of this layer. Useful to add custom origins to the default origin layer for example. If set to true, the layer will be replaced and only the origins specified in this file will appear.
`name` | [String](../types/data_types/string.md) | _optional_ | The display name of the layer. Will show at the top of the GUI saying "Choose your [name here]". Can be a literal string or a translation key.
`gui_title` | [GUI Title](../types/data_types/gui_title.md) | _optional_ | If specified, the choose/view origin title for the layer (the text that shows at the top of the GUI) will be overridden by this.
`missing_name` | [String](../types/data_types/string.md) | _optional_ | The display name of the origin that will show when viewing the origin if no origin has been assigned to this layer. Can be a literal string or a translation key.
`missing_description` | [String](../types/data_types/string.md) | _optional_ | The description of the origin that will show when viewing the origin if no origin has been assigned to this layer. Can be a literal string or a translation key.
`allow_random` | [Boolean](../types/data_types/boolean.md) | `false` | If set to true, this layer will show an option for choosing a random origin.
`allow_random_unchoosable` | [Boolean](../types/data_types/boolean.md) | `false` | Whether origins which are unchoosable (`unchoosable` field set to true in the origin file) should be included in the random option. Can for example be used to force players to choose a random origin, by setting this to true and making all origins in the layer unchoosable.
`exclude_random` | [Array](../types/data_types/array.md) of [Identifiers](../types/data_types/identifier.md) | _optional_ | If specified, the origins included in this list will not be picked by the random choice.
`default_origin` | [Identifier](../types/data_types/identifier.md) | _optional_ | If set, the origin with this namespace and ID will automatically be chosen for a new player. If an orb of origin is used later on, the player will be able to choose another origin then and the `default_origin` will not apply. Could for example be used to make all players start as human, and then use the orb as a progression item to select an origin.
`auto_choose` | [Boolean](../types/data_types/boolean.md) | `false` | If set to true, this layer will automatically pick an origin for the player if only one option is available. This also applies when an orb of origin is used.
`hidden` | [Boolean](../types/data_types/boolean.md) | `false` | If set to true, this layer will be hidden from the "View Origin" screen.
`loading_priority` | [Integer](../types/data_types/integer.md) | `0` | Specifies when this layer is loaded. Higher numbers mean it's loaded later, which means it will override those with lower loading priorities which share the same ID.



### Examples

```json
{
    "order": 1,
    "origins": [
        "origins:arachnid",
        "origins:avian",
        "origins:blazeborn",
        "origins:elytrian",
        "origins:enderian",
        "origins:feline",
        "origins:human",
        "origins:merling",
        "origins:phantom",
        "origins:shulk"
    ],
    "name": "Second Origin",
    "missing_name": "None",
    "missing_description": "You currently don't have a secondary origin selected."
}
```

This example will make it possible to select a secondary base origin after choosing an origin in the `origins:origin` (`data/origins/origin_layers/origin.json`) origin layer as long as the example is a separate origin layer.
