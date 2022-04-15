---
title: GUI Title (Data Types)
date: 2022-04-15
---

# GUI Title

[Data Type](../data_types.md)

An [object](object.md) used to override the title in the choose/view origin GUI of a layer.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`choose_origin` | [String](string.md) | _optional_ | If specified, this will override the title that shows up when choosing an origin in the layer.
`view_origin` | [String](string.md) | _optional_ | If specified, this will override the title that shows up when viewing an origin in the layer.


### Examples

```json
"gui_title": {
    "choose_origin": "Choose your stuff!",
    "view_origin": "This is the stuff that you chose."
}
```

This example will make the origin layer show *"Choose your stuff!"* in the prompt for choosing an origin in the layer, and *"This is the stuff that you chose."* in the prompt for viewing an origin in the layer.
