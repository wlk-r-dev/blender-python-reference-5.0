# UILayout(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.UILayout(_bpy_struct_)
    

User interface layout in a panel or header

activate_init
    

When true, buttons defined in popups will be activated on first display (use so you can type into a field without having to click on it first)

Type:
    

boolean, default False

active
    

Type:
    

boolean, default False

active_default
    

When true, an operator button defined after this will be activated when pressing return(use with popup dialogs)

Type:
    

boolean, default False

alert
    

Type:
    

boolean, default False

alignment
    

Type:
    

enum in [`'EXPAND'`, `'LEFT'`, `'CENTER'`, `'RIGHT'`], default `'EXPAND'`

direction
    

Type:
    

enum in [`'HORIZONTAL'`, `'VERTICAL'`], default `'HORIZONTAL'`, (readonly)

emboss
    

  * `NORMAL` Regular – Draw standard button emboss style.

  * `NONE` None – Draw only text and icons.

  * `PULLDOWN_MENU` Pull-down Menu – Draw pull-down menu style.

  * `PIE_MENU` Pie Menu – Draw radial menu style.

  * `NONE_OR_STATUS` None or Status – Draw with no emboss unless the button has a coloring status like an animation state.


Type:
    

enum in [`'NORMAL'`, `'NONE'`, `'PULLDOWN_MENU'`, `'PIE_MENU'`, `'NONE_OR_STATUS'`], default `'NORMAL'`

enabled
    

When false, this (sub)layout is grayed out

Type:
    

boolean, default False

operator_context
    

Typically set to ‘INVOKE_REGION_WIN’, except some cases in [`bpy.types.Menu`](../M/bpy.types.Menu.md#bpy.types.Menu "bpy.types.Menu") when it’s set to ‘EXEC_REGION_WIN’.

Type:
    

enum in [Operator Context Items](../../bpy_types_enum_items/operator_context_items.md#rna-enum-operator-context-items), default `'INVOKE_DEFAULT'`

scale_x
    

Scale factor along the X for items in this (sub)layout

Type:
    

float in [0, inf], default 0.0

scale_y
    

Scale factor along the Y for items in this (sub)layout

Type:
    

float in [0, inf], default 0.0

ui_units_x
    

Fixed size along the X for items in this (sub)layout

Type:
    

float in [0, inf], default 0.0

ui_units_y
    

Fixed size along the Y for items in this (sub)layout

Type:
    

float in [0, inf], default 0.0

use_property_decorate
    

Type:
    

boolean, default False

use_property_split
    

Type:
    

boolean, default False

row(_*_ , _align =False_, _heading =''_, _heading_ctxt =''_, _translate =True_)
    

Sub-layout. Items placed in this sublayout are placed next to each other in a row.

Parameters:
    

  * **align** (_boolean_ _,__(__optional_ _)_) – Align buttons to each other

  * **heading** (_string_ _,__(__optional_ _,__never None_ _)_) – Heading, Label to insert into the layout for this sub-layout

  * **heading_ctxt** (_string_ _,__(__optional_ _,__never None_ _)_) – Override automatic translation context of the given heading

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given heading, when UI translation is enabled


Returns:
    

Sub-layout to put items in

Return type:
    

`UILayout`

column(_*_ , _align =False_, _heading =''_, _heading_ctxt =''_, _translate =True_)
    

Sub-layout. Items placed in this sublayout are placed under each other in a column.

Parameters:
    

  * **align** (_boolean_ _,__(__optional_ _)_) – Align buttons to each other

  * **heading** (_string_ _,__(__optional_ _,__never None_ _)_) – Heading, Label to insert into the layout for this sub-layout

  * **heading_ctxt** (_string_ _,__(__optional_ _,__never None_ _)_) – Override automatic translation context of the given heading

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given heading, when UI translation is enabled


Returns:
    

Sub-layout to put items in

Return type:
    

`UILayout`

panel(_idname_ , _*_ , _default_closed =False_)
    

Creates a collapsible panel. Whether it is open or closed is stored in the region using the given idname. This can only be used when the panel has the full width of the panel region available to it. So it can’t be used in e.g. in a box or columns.

Parameters:
    

  * **idname** (_string_ _,__(__never None_ _)_) – Identifier of the panel

  * **default_closed** (_boolean_ _,__(__optional_ _)_) – Open by Default, When true, the panel will be open the first time it is shown


Returns:
    

`layout_header`, Sub-layout to put items in, `UILayout`

`layout_body`, Sub-layout to put items in. Will be none if the panel is collapsed., `UILayout`

Return type:
    

(`UILayout`, `UILayout`)

panel_prop(_data_ , _property_)
    

Similar to `.panel(...)` but instead of storing whether it is open or closed in the region, it is stored in the provided boolean property. This should be used when multiple instances of the same panel can exist. For example one for every item in a collection property or list. This can only be used when the panel has the full width of the panel region available to it. So it can’t be used in e.g. in a box or columns.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take the open-state property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of the boolean property that determines whether the panel is open or closed


Returns:
    

`layout_header`, Sub-layout to put items in, `UILayout`

`layout_body`, Sub-layout to put items in. Will be none if the panel is collapsed., `UILayout`

Return type:
    

(`UILayout`, `UILayout`)

column_flow(_*_ , _columns =0_, _align =False_)
    

column_flow

Parameters:
    

  * **columns** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Number of columns, 0 is automatic

  * **align** (_boolean_ _,__(__optional_ _)_) – Align buttons to each other


Returns:
    

Sub-layout to put items in

Return type:
    

`UILayout`

grid_flow(_*_ , _row_major =False_, _columns =0_, _even_columns =False_, _even_rows =False_, _align =False_)
    

grid_flow

Parameters:
    

  * **row_major** (_boolean_ _,__(__optional_ _)_) – Fill row by row, instead of column by column

  * **columns** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Number of columns, positive are absolute fixed numbers, 0 is automatic, negative are automatic multiple numbers along major axis (e.g. -2 will only produce 2, 4, 6 etc. columns for row major layout, and 2, 4, 6 etc. rows for column major layout).

  * **even_columns** (_boolean_ _,__(__optional_ _)_) – All columns will have the same width

  * **even_rows** (_boolean_ _,__(__optional_ _)_) – All rows will have the same height

  * **align** (_boolean_ _,__(__optional_ _)_) – Align buttons to each other


Returns:
    

Sub-layout to put items in

Return type:
    

`UILayout`

box()
    

Sublayout (items placed in this sublayout are placed under each other in a column and are surrounded by a box)

Returns:
    

Sub-layout to put items in

Return type:
    

`UILayout`

split(_*_ , _factor =0.0_, _align =False_)
    

split

Parameters:
    

  * **factor** (_float in_ _[__0_ _,__1_ _]__,__(__optional_ _)_) – Percentage, Percentage of width to split at (leave unset for automatic calculation)

  * **align** (_boolean_ _,__(__optional_ _)_) – Align buttons to each other


Returns:
    

Sub-layout to put items in

Return type:
    

`UILayout`

menu_pie()
    

Sublayout. Items placed in this sublayout are placed in a radial fashion around the menu center).

Returns:
    

Sub-layout to put items in

Return type:
    

`UILayout`

_classmethod _icon(_data_)
    

Return the custom icon for this data, use it e.g. to get materials or texture icons.

Parameters:
    

**data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take the icon

Returns:
    

Icon identifier

Return type:
    

int in [0, inf]

_classmethod _enum_item_name(_data_ , _property_ , _identifier_)
    

Return the UI name for this enum item

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **identifier** (_string_ _,__(__never None_ _)_) – Identifier of the enum item


Returns:
    

UI name of the enum item

Return type:
    

string, (never None)

_classmethod _enum_item_description(_data_ , _property_ , _identifier_)
    

Return the UI description for this enum item

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **identifier** (_string_ _,__(__never None_ _)_) – Identifier of the enum item


Returns:
    

UI description of the enum item

Return type:
    

string, (never None)

_classmethod _enum_item_icon(_data_ , _property_ , _identifier_)
    

Return the icon for this enum item

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **identifier** (_string_ _,__(__never None_ _)_) – Identifier of the enum item


Returns:
    

Icon identifier

Return type:
    

int in [0, inf]

prop(_data_ , _property_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _placeholder =''_, _expand =False_, _slider =False_, _toggle =-1_, _icon_only =False_, _event =False_, _full_event =False_, _emboss =True_, _index =-1_, _icon_value =0_, _invert_checkbox =False_)
    

Item. Exposes an RNA item and places it into the layout.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **placeholder** (_string_ _,__(__optional_ _)_) – Hint describing the expected value when empty

  * **expand** (_boolean_ _,__(__optional_ _)_) – Expand button to show more detail

  * **slider** (_boolean_ _,__(__optional_ _)_) – Use slider widget for numeric values

  * **toggle** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – Use toggle widget for boolean values, or a checkbox when disabled (the default is -1 which uses toggle only when an icon is displayed)

  * **icon_only** (_boolean_ _,__(__optional_ _)_) – Draw only icons in buttons, no text

  * **event** (_boolean_ _,__(__optional_ _)_) – Use button to input key events

  * **full_event** (_boolean_ _,__(__optional_ _)_) – Use button to input full events including modifiers

  * **emboss** (_boolean_ _,__(__optional_ _)_) – Draw the button itself, not just the icon/text. When false, corresponds to the ‘NONE_OR_STATUS’ layout emboss type.

  * **index** (_int in_ _[__-2_ _,__inf_ _]__,__(__optional_ _)_) – The index of this button, when set a single member of an array can be accessed, when set to -1 all array members are used

  * **icon_value** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Icon Value, Override automatic icon of the item

  * **invert_checkbox** (_boolean_ _,__(__optional_ _)_) – Draw checkbox value inverted


props_enum(_data_ , _property_)
    

props_enum

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


prop_menu_enum(_data_ , _property_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_)
    

prop_menu_enum

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item


prop_with_popover(_data_ , _property_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _icon_only =False_, _panel_)
    

prop_with_popover

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **icon_only** (_boolean_ _,__(__optional_ _)_) – Draw only icons in tabs, no text

  * **panel** (_string_ _,__(__never None_ _)_) – Identifier of the panel


prop_with_menu(_data_ , _property_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _icon_only =False_, _menu_)
    

prop_with_menu

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **icon_only** (_boolean_ _,__(__optional_ _)_) – Draw only icons in tabs, no text

  * **menu** (_string_ _,__(__never None_ _)_) – Identifier of the menu


prop_tabs_enum(_data_ , _property_ , _*_ , _data_highlight =None_, _property_highlight =''_, _icon_only =False_)
    

prop_tabs_enum

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **data_highlight** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (optional, never None)) – Data from which to take highlight property

  * **property_highlight** (_string_ _,__(__optional_ _,__never None_ _)_) – Identifier of highlight property in data

  * **icon_only** (_boolean_ _,__(__optional_ _)_) – Draw only icons in tabs, no text


prop_enum(_data_ , _property_ , _value_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_)
    

prop_enum

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **value** (_string_ _,__(__never None_ _)_) – Enum property value

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item


prop_search(_data_ , _property_ , _search_data_ , _search_property_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _results_are_suggestions =False_, _item_search_property =''_)
    

prop_search

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **search_data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take collection to search in

  * **search_property** (_string_ _,__(__never None_ _)_) – Identifier of search collection property

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **results_are_suggestions** (_boolean_ _,__(__optional_ _)_) – Accept inputs that do not match any item

  * **item_search_property** (_string_ _,__(__optional_ _,__never None_ _)_) – Identifier of the string property in each collection’s items to use for searching (defaults to the items’ type ‘name property’)


prop_decorator(_data_ , _property_ , _*_ , _index =-1_)
    

prop_decorator

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **index** (_int in_ _[__-2_ _,__inf_ _]__,__(__optional_ _)_) – The index of this button, when set a single member of an array can be accessed, when set to -1 all array members are used


operator(_operator_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _emboss =True_, _depress =False_, _icon_value =0_, _search_weight =0.0_)
    

Item. Places a button into the layout to call an Operator.

Parameters:
    

  * **operator** (_string_ _,__(__never None_ _)_) – Identifier of the operator

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **emboss** (_boolean_ _,__(__optional_ _)_) – Draw the button itself, not just the icon/text

  * **depress** (_boolean_ _,__(__optional_ _)_) – Draw pressed in

  * **icon_value** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Icon Value, Override automatic icon of the item

  * **search_weight** (_float in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Search Weight, Influences the sorting when using menu-seach


Returns:
    

Operator properties to fill in

Return type:
    

[`OperatorProperties`](../O/bpy.types.OperatorProperties.md#bpy.types.OperatorProperties "bpy.types.OperatorProperties")

operator_menu_hold(_operator_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _emboss =True_, _depress =False_, _icon_value =0_, _menu_)
    

Item. Places a button into the layout to call an Operator.

Parameters:
    

  * **operator** (_string_ _,__(__never None_ _)_) – Identifier of the operator

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **emboss** (_boolean_ _,__(__optional_ _)_) – Draw the button itself, not just the icon/text

  * **depress** (_boolean_ _,__(__optional_ _)_) – Draw pressed in

  * **icon_value** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Icon Value, Override automatic icon of the item

  * **menu** (_string_ _,__(__never None_ _)_) – Identifier of the menu


Returns:
    

Operator properties to fill in

Return type:
    

[`OperatorProperties`](../O/bpy.types.OperatorProperties.md#bpy.types.OperatorProperties "bpy.types.OperatorProperties")

operator_enum(_operator_ , _property_ , _*_ , _icon_only =False_)
    

operator_enum

Parameters:
    

  * **operator** (_string_ _,__(__never None_ _)_) – Identifier of the operator

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in operator

  * **icon_only** (_boolean_ _,__(__optional_ _)_) – Draw only icons in buttons, no text


operator_menu_enum(_operator_ , _property_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_)
    

operator_menu_enum

Parameters:
    

  * **operator** (_string_ _,__(__never None_ _)_) – Identifier of the operator

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in operator

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item


Returns:
    

Operator properties to fill in

Return type:
    

[`OperatorProperties`](../O/bpy.types.OperatorProperties.md#bpy.types.OperatorProperties "bpy.types.OperatorProperties")

label(_*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _icon_value =0_)
    

Item. Displays text and/or icon in the layout.

Parameters:
    

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **icon_value** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Icon Value, Override automatic icon of the item


menu(_menu_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _icon_value =0_)
    

menu

Parameters:
    

  * **menu** (_string_ _,__(__never None_ _)_) – Identifier of the menu

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **icon_value** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Icon Value, Override automatic icon of the item


menu_contents(_menu_)
    

menu_contents

Parameters:
    

**menu** (_string_ _,__(__never None_ _)_) – Identifier of the menu

popover(_panel_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _icon_value =0_)
    

popover

Parameters:
    

  * **panel** (_string_ _,__(__never None_ _)_) – Identifier of the panel

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **icon_value** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Icon Value, Override automatic icon of the item


popover_group(_space_type_ , _region_type_ , _context_ , _category_)
    

popover_group

Parameters:
    

  * **space_type** (enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items)) – Space Type

  * **region_type** (enum in [Region Type Items](../../bpy_types_enum_items/region_type_items.md#rna-enum-region-type-items)) – Region Type

  * **context** (_string_ _,__(__never None_ _)_) – panel type context

  * **category** (_string_ _,__(__never None_ _)_) – panel type category


separator(_*_ , _factor =1.0_, _type ='AUTO'_)
    

Item. Inserts empty space into the layout between items.

Parameters:
    

  * **factor** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Percentage, Percentage of width to space (leave unset for default space)

  * **type** (enum in [`'AUTO'`, `'SPACE'`, `'LINE'`], (optional)) – 

Type, The type of the separator

    * `AUTO` Auto – Best guess at what type of separator is needed..

    * `SPACE` Empty space – Horizontal or Vertical empty space, depending on layout direction..

    * `LINE` Line – Horizontal or Vertical line, depending on layout direction..


separator_spacer()
    

Item. Inserts horizontal spacing empty space into the layout between items.

progress(_*_ , _text =''_, _text_ctxt =''_, _translate =True_, _factor =0.0_, _type ='BAR'_)
    

Progress indicator

Parameters:
    

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **factor** (_float in_ _[__0_ _,__1_ _]__,__(__optional_ _)_) – Factor, Amount of progress from 0.0f to 1.0f

  * **type** (enum in [`'BAR'`, `'RING'`], (optional)) – Type, The type of progress indicator


context_pointer_set(_name_ , _data_)
    

context_pointer_set

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name, Name of entry in the context

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType")) – Pointer to put in context


context_string_set(_name_ , _value_)
    

context_string_set

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name, Name of entry in the context

  * **value** (_string_ _,__(__never None_ _)_) – Value, String to put in context


template_header()
    

Inserts common Space header UI (editor type selector)

template_ID(_data_ , _property_ , _*_ , _new =''_, _open =''_, _unlink =''_, _filter ='ALL'_, _live_icon =False_, _text =''_, _text_ctxt =''_, _translate =True_)
    

template_ID

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **new** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to create a new ID block

  * **open** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to open a file for creating a new ID block

  * **unlink** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to unlink the ID block

  * **filter** (enum in [`'ALL'`, `'AVAILABLE'`], (optional)) – Optionally limit the items which can be selected

  * **live_icon** (_boolean_ _,__(__optional_ _)_) – Show preview instead of fixed icon

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled


template_ID_preview(_data_ , _property_ , _*_ , _new =''_, _open =''_, _unlink =''_, _rows =0_, _cols =0_, _filter ='ALL'_, _hide_buttons =False_)
    

template_ID_preview

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **new** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to create a new ID block

  * **open** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to open a file for creating a new ID block

  * **unlink** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to unlink the ID block

  * **rows** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Number of thumbnail preview rows to display

  * **cols** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Number of thumbnail preview columns to display

  * **filter** (enum in [`'ALL'`, `'AVAILABLE'`], (optional)) – Optionally limit the items which can be selected

  * **hide_buttons** (_boolean_ _,__(__optional_ _)_) – Show only list, no buttons


template_matrix(_data_ , _property_)
    

Insert a readonly Matrix UI. The UI displays the matrix components - translation, rotation and scale. The **property** argument must be the identifier of an existing 4x4 float vector property of subtype ‘MATRIX’.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_any_ID(_data_ , _property_ , _type_property_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_)
    

template_any_ID

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **type_property** (_string_ _,__(__never None_ _)_) – Identifier of property in data giving the type of the ID-blocks to use

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled


template_ID_tabs(_data_ , _property_ , _*_ , _new =''_, _menu =''_, _filter ='ALL'_)
    

template_ID_tabs

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **new** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to create a new ID block

  * **menu** (_string_ _,__(__optional_ _,__never None_ _)_) – Context menu identifier

  * **filter** (enum in [`'ALL'`, `'AVAILABLE'`], (optional)) – Optionally limit the items which can be selected


template_action(_id_ , _*_ , _new =''_, _unlink =''_, _text =''_, _text_ctxt =''_, _translate =True_)
    

template_action

Parameters:
    

  * **id** ([`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), (never None)) – The data-block for which to select an Action

  * **new** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to create a new ID block

  * **unlink** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to unlink the ID block

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled


template_search(_data_ , _property_ , _search_data_ , _search_property_ , _*_ , _new =''_, _unlink =''_, _text =''_, _text_ctxt =''_, _translate =True_)
    

template_search

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **search_data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take collection to search in

  * **search_property** (_string_ _,__(__never None_ _)_) – Identifier of search collection property

  * **new** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to create a new item for the collection

  * **unlink** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to unlink or delete the active item from the collection

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled


template_search_preview(_data_ , _property_ , _search_data_ , _search_property_ , _*_ , _new =''_, _unlink =''_, _text =''_, _text_ctxt =''_, _translate =True_, _rows =0_, _cols =0_)
    

template_search_preview

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **search_data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take collection to search in

  * **search_property** (_string_ _,__(__never None_ _)_) – Identifier of search collection property

  * **new** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to create a new item for the collection

  * **unlink** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator identifier to unlink or delete the active item from the collection

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **rows** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Number of thumbnail preview rows to display

  * **cols** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Number of thumbnail preview columns to display


template_path_builder(_data_ , _property_ , _root_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_)
    

template_path_builder

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **root** ([`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")) – ID-block from which path is evaluated from

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled


template_modifiers()
    

Generates the UI layout for the modifier stack

template_strip_modifiers()
    

Generates the UI layout for the strip modifier stack

template_collection_exporters()
    

Generates the UI layout for collection exporters

template_constraints(_*_ , _use_bone_constraints =True_)
    

Generates the panels for the constraint stack

Parameters:
    

**use_bone_constraints** (_boolean_ _,__(__optional_ _)_) – Add panels for bone constraints instead of object constraints

template_shaderfx()
    

Generates the panels for the shader effect stack

template_greasepencil_color(_data_ , _property_ , _*_ , _rows =0_, _cols =0_, _scale =1.0_, _filter ='ALL'_)
    

template_greasepencil_color

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **rows** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Number of thumbnail preview rows to display

  * **cols** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Number of thumbnail preview columns to display

  * **scale** (_float in_ _[__0.1_ _,__1.5_ _]__,__(__optional_ _)_) – Scale of the image thumbnails

  * **filter** (enum in [`'ALL'`, `'AVAILABLE'`], (optional)) – Optionally limit the items which can be selected


template_constraint_header(_data_)
    

Generates the header for constraint panels

Parameters:
    

**data** ([`Constraint`](../C/bpy.types.Constraint.md#bpy.types.Constraint "bpy.types.Constraint"), (never None)) – Constraint data

template_preview(_id_ , _*_ , _show_buttons =True_, _parent =None_, _slot =None_, _preview_id =''_)
    

Item. A preview window for materials, textures, lights or worlds.

Parameters:
    

  * **id** ([`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")) – ID data-block

  * **show_buttons** (_boolean_ _,__(__optional_ _)_) – Show preview buttons?

  * **parent** ([`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), (optional)) – ID data-block

  * **slot** ([`TextureSlot`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot "bpy.types.TextureSlot"), (optional)) – Texture slot

  * **preview_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Identifier of this preview widget, if not set the ID type will be used (i.e. all previews of materials without explicit ID will have the same size…).


template_curve_mapping(_data_ , _property_ , _*_ , _type ='NONE'_, _levels =False_, _brush =False_, _use_negative_slope =False_, _show_tone =False_, _show_presets =False_)
    

Item. A curve mapping widget used for e.g falloff curves for lights.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **type** (enum in [`'NONE'`, `'VECTOR'`, `'COLOR'`, `'HUE'`], (optional)) – Type, Type of curves to display

  * **levels** (_boolean_ _,__(__optional_ _)_) – Show black/white levels

  * **brush** (_boolean_ _,__(__optional_ _)_) – Show brush options

  * **use_negative_slope** (_boolean_ _,__(__optional_ _)_) – Use a negative slope by default

  * **show_tone** (_boolean_ _,__(__optional_ _)_) – Show tone options

  * **show_presets** (_boolean_ _,__(__optional_ _)_) – Show preset options


template_curveprofile(_data_ , _property_)
    

A profile path editor used for custom profiles

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_color_ramp(_data_ , _property_ , _*_ , _expand =False_)
    

Item. A color ramp widget.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **expand** (_boolean_ _,__(__optional_ _)_) – Expand button to show more detail


template_icon(_icon_value_ , _*_ , _scale =1.0_)
    

Display a large icon

Parameters:
    

  * **icon_value** (_int in_ _[__0_ _,__inf_ _]_) – Icon to display

  * **scale** (_float in_ _[__1_ _,__100_ _]__,__(__optional_ _)_) – Scale, Scale the icon size (by the button size)


template_icon_view(_data_ , _property_ , _*_ , _show_labels =False_, _scale =6.0_, _scale_popup =5.0_)
    

Enum. Large widget showing Icon previews.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **show_labels** (_boolean_ _,__(__optional_ _)_) – Show enum label in preview buttons

  * **scale** (_float in_ _[__1_ _,__100_ _]__,__(__optional_ _)_) – UI Units, Scale the button icon size (by the button size)

  * **scale_popup** (_float in_ _[__1_ _,__100_ _]__,__(__optional_ _)_) – Scale, Scale the popup icon size (by the button size)


template_histogram(_data_ , _property_)
    

Item. A histogramm widget to analyze imaga data.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_waveform(_data_ , _property_)
    

Item. A waveform widget to analyze imaga data.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_vectorscope(_data_ , _property_)
    

Item. A vectorscope widget to analyze imaga data.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_layers(_data_ , _property_ , _used_layers_data_ , _used_layers_property_ , _active_layer_)
    

template_layers

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **used_layers_data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType")) – Data from which to take property

  * **used_layers_property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **active_layer** (_int in_ _[__0_ _,__inf_ _]_) – Active Layer


template_color_picker(_data_ , _property_ , _*_ , _value_slider =False_, _lock =False_, _lock_luminosity =False_, _cubic =False_)
    

Item. A color wheel widget to pick colors.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **value_slider** (_boolean_ _,__(__optional_ _)_) – Display the value slider to the right of the color wheel

  * **lock** (_boolean_ _,__(__optional_ _)_) – Lock the color wheel display to value 1.0 regardless of actual color

  * **lock_luminosity** (_boolean_ _,__(__optional_ _)_) – Keep the color at its original vector length

  * **cubic** (_boolean_ _,__(__optional_ _)_) – Cubic saturation for picking values close to white


template_palette(_data_ , _property_ , _*_ , _color =False_)
    

Item. A palette used to pick colors.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **color** (_boolean_ _,__(__optional_ _)_) – Display the colors as colors or values


template_image_layers(_image_ , _image_user_)
    

template_image_layers

template_image(_data_ , _property_ , _image_user_ , _*_ , _compact =False_, _multiview =False_)
    

Item(s). User interface for selecting images and their source paths.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **compact** (_boolean_ _,__(__optional_ _)_) – Use more compact layout

  * **multiview** (_boolean_ _,__(__optional_ _)_) – Expose Multi-View options


template_image_settings(_image_settings_ , _*_ , _color_management =False_)
    

User interface for setting image format options

Parameters:
    

**color_management** (_boolean_ _,__(__optional_ _)_) – Show color management settings

template_image_stereo_3d(_stereo_3d_format_)
    

User interface for setting image stereo 3d options

template_image_views(_image_settings_)
    

User interface for setting image views output options

template_movieclip(_data_ , _property_ , _*_ , _compact =False_)
    

Item(s). User interface for selecting movie clips and their source paths.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **compact** (_boolean_ _,__(__optional_ _)_) – Use more compact layout


template_track(_data_ , _property_)
    

Item. A movie-track widget to preview tracking image.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_marker(_data_ , _property_ , _clip_user_ , _track_ , _*_ , _compact =False_)
    

Item. A widget to control single marker settings.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data

  * **compact** (_boolean_ _,__(__optional_ _)_) – Use more compact layout


template_movieclip_information(_data_ , _property_ , _clip_user_)
    

Item. Movie clip information data.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_list(_listtype_name_ , _list_id_ , _dataptr_ , _propname_ , _active_dataptr_ , _active_propname_ , _*_ , _item_dyntip_propname =''_, _rows =5_, _maxrows =5_, _type ='DEFAULT'_, _columns =9_, _sort_reverse =False_, _sort_lock =False_)
    

Item. A list widget to display data, e.g. vertexgroups.

Parameters:
    

  * **listtype_name** (_string_ _,__(__never None_ _)_) – Identifier of the list type to use

  * **list_id** (_string_ _,__(__never None_ _)_) – Identifier of this list widget. Necessary to tell apart different list widgets. Mandatory when using default “UI_UL_list” class. If this not an empty string, the uilist gets a custom ID, otherwise it takes the name of the class used to define the uilist (for example, if the class name is “OBJECT_UL_vgroups”, and list_id is not set by the script, then bl_idname = “OBJECT_UL_vgroups”)

  * **dataptr** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType")) – Data from which to take the Collection property

  * **propname** (_string_ _,__(__never None_ _)_) – Identifier of the Collection property in data

  * **active_dataptr** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take the integer property, index of the active item

  * **active_propname** (_string_ _,__(__never None_ _)_) – Identifier of the integer property in active_data, index of the active item

  * **item_dyntip_propname** (_string_ _,__(__optional_ _,__never None_ _)_) – Identifier of a string property in items, to use as tooltip content

  * **rows** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Default and minimum number of rows to display

  * **maxrows** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Default maximum number of rows to display

  * **type** (enum in [Uilist Layout Type Items](../../bpy_types_enum_items/uilist_layout_type_items.md#rna-enum-uilist-layout-type-items), (optional)) – Type, Type of layout to use

  * **columns** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Number of items to display per row, for GRID layout

  * **sort_reverse** (_boolean_ _,__(__optional_ _)_) – Display items in reverse order by default

  * **sort_lock** (_boolean_ _,__(__optional_ _)_) – Lock display order to default value


template_running_jobs()
    

template_running_jobs

template_operator_search()
    

template_operator_search

template_menu_search()
    

template_menu_search

template_header_3D_mode()
    

template_edit_mode_selection()
    

Inserts common 3DView Edit modes header UI (selector for selection mode)

template_reports_banner()
    

template_reports_banner

template_input_status()
    

template_input_status

template_status_info()
    

template_status_info

template_node_link(_ntree_ , _node_ , _socket_)
    

template_node_link

template_node_view(_ntree_ , _node_ , _socket_)
    

template_node_view

template_node_asset_menu_items(_*_ , _catalog_path =''_, _operator ='ADD'_)
    

template_node_asset_menu_items

Parameters:
    

**operator** (enum in [`'ADD'`, `'SWAP'`], (optional)) – 

Operator, The operator the asset menu will use

  * `ADD` Add Node – Add a node to the active tree..

  * `SWAP` Swap Node – Replace the selected nodes with the specified type..


template_modifier_asset_menu_items(_*_ , _catalog_path =''_, _skip_essentials =False_)
    

template_modifier_asset_menu_items

template_node_operator_asset_menu_items(_*_ , _catalog_path =''_)
    

template_node_operator_asset_menu_items

template_node_operator_asset_root_items()
    

template_node_operator_asset_root_items

template_texture_user()
    

template_texture_user

template_keymap_item_properties(_item_)
    

template_keymap_item_properties

template_component_menu(_data_ , _property_ , _*_ , _name =''_)
    

Item. Display expanded property in a popup menu

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType")) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_colorspace_settings(_data_ , _property_)
    

Item. A widget to control input color space settings.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_colormanaged_view_settings(_data_ , _property_)
    

Item. A widget to control color managed view settings.

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_node_socket(_*_ , _color =(0.0, 0.0, 0.0, 1.0)_)
    

Node Socket Icon

Parameters:
    

**color** (_float array_ _of_ _4 items in_ _[__0_ _,__1_ _]__,__(__optional_ _)_) – Color

template_cache_file(_data_ , _property_)
    

Item(s). User interface for selecting cache files and their source paths

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_cache_file_velocity(_data_ , _property_)
    

Show cache files velocity properties

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_cache_file_time_settings(_data_ , _property_)
    

Show cache files time settings

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_cache_file_layers(_data_ , _property_)
    

Show cache files override layers properties

Parameters:
    

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_recent_files(_*_ , _rows =6_)
    

Show list of recently saved .blend files

Parameters:
    

**rows** (_int in_ _[__1_ _,__inf_ _]__,__(__optional_ _)_) – Maximum number of items to show

Returns:
    

Number of items drawn

Return type:
    

int in [0, inf]

template_file_select_path(_params_)
    

Item. A text button to set the active file browser path.

template_event_from_keymap_item(_item_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_)
    

Display keymap item as icons/text

Parameters:
    

  * **item** ([`KeyMapItem`](../K/bpy.types.KeyMapItem.md#bpy.types.KeyMapItem "bpy.types.KeyMapItem"), (never None)) – Item

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled


template_light_linking_collection(_context_layout_ , _data_ , _property_)
    

Visualization of a content of a light linking collection

Parameters:
    

  * **context_layout** (`UILayout`, (never None)) – Layout to set active list element as context properties

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


template_bone_collection_tree()
    

Show bone collections tree

template_grease_pencil_layer_tree()
    

View of the active Grease Pencil layer tree

template_node_tree_interface(_interface_)
    

Show a node tree interface

Parameters:
    

**interface** ([`NodeTreeInterface`](../N/bpy.types.NodeTreeInterface.md#bpy.types.NodeTreeInterface "bpy.types.NodeTreeInterface"), (never None)) – Node Tree Interface, Interface of a node tree to display

template_node_inputs(_node_)
    

Show a node settings and input socket values

Parameters:
    

**node** ([`Node`](../N/bpy.types.Node.md#bpy.types.Node "bpy.types.Node"), (never None)) – Node, Display inputs of this node

template_asset_shelf_popover(_asset_shelf_ , _*_ , _name =''_, _icon ='NONE'_, _icon_value =0_)
    

Create a button to open an asset shelf in a popover

Parameters:
    

  * **asset_shelf** (_string_ _,__(__never None_ _)_) – Identifier of the asset shelf to display (`bl_idname`)

  * **name** (_string_ _,__(__optional_ _)_) – Optional name to indicate the active asset

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **icon_value** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Icon Value, Override automatic icon of the item


template_popup_confirm(_operator_ , _*_ , _text =''_, _text_ctxt =''_, _translate =True_, _icon ='NONE'_, _cancel_text =''_, _cancel_default =False_)
    

Add confirm & cancel buttons into a popup which will close the popup when pressed

Parameters:
    

  * **operator** (_string_ _,__(__never None_ _)_) – Identifier of the operator

  * **text** (_string_ _,__(__optional_ _)_) – Override automatic text of the item

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled

  * **icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – Icon, Override automatic icon of the item

  * **cancel_text** (_string_ _,__(__optional_ _,__never None_ _)_) – Optional text to use for the cancel, not shown when an empty string

  * **cancel_default** (_boolean_ _,__(__optional_ _)_) – Cancel button by default


Returns:
    

Operator properties to fill in

Return type:
    

[`OperatorProperties`](../O/bpy.types.OperatorProperties.md#bpy.types.OperatorProperties "bpy.types.OperatorProperties")

template_shape_key_tree()
    

Shape Key tree view

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

introspect()
    

Return a list of dictionaries containing a textual representation of the UI layout.

Return type:
    

list[dict[str, Any]]

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`AssetShelf.draw_context_menu`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.draw_context_menu "bpy.types.AssetShelf.draw_context_menu")
  * [`Header.layout`](../H/bpy.types.Header.md#bpy.types.Header.layout "bpy.types.Header.layout")
  * [`Menu.layout`](../M/bpy.types.Menu.md#bpy.types.Menu.layout "bpy.types.Menu.layout")
  * [`Node.draw_buttons`](../N/bpy.types.Node.md#bpy.types.Node.draw_buttons "bpy.types.Node.draw_buttons")
  * [`Node.draw_buttons_ext`](../N/bpy.types.Node.md#bpy.types.Node.draw_buttons_ext "bpy.types.Node.draw_buttons_ext")
  * [`NodeInternal.draw_buttons`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.draw_buttons "bpy.types.NodeInternal.draw_buttons")
  * [`NodeInternal.draw_buttons_ext`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.draw_buttons_ext "bpy.types.NodeInternal.draw_buttons_ext")
  * [`NodeSocket.draw`](../N/bpy.types.NodeSocket.md#bpy.types.NodeSocket.draw "bpy.types.NodeSocket.draw")
  * [`NodeSocketStandard.draw`](../N/bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard.draw "bpy.types.NodeSocketStandard.draw")
  * [`NodeTreeInterfaceSocket.draw`](../N/bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.draw "bpy.types.NodeTreeInterfaceSocket.draw")
  * [`NodeTreeInterfaceSocketBool.draw`](../N/bpy.types.NodeTreeInterfaceSocketBool.md#bpy.types.NodeTreeInterfaceSocketBool.draw "bpy.types.NodeTreeInterfaceSocketBool.draw")
  * [`NodeTreeInterfaceSocketBundle.draw`](../N/bpy.types.NodeTreeInterfaceSocketBundle.md#bpy.types.NodeTreeInterfaceSocketBundle.draw "bpy.types.NodeTreeInterfaceSocketBundle.draw")
  * [`NodeTreeInterfaceSocketClosure.draw`](../N/bpy.types.NodeTreeInterfaceSocketClosure.md#bpy.types.NodeTreeInterfaceSocketClosure.draw "bpy.types.NodeTreeInterfaceSocketClosure.draw")
  * [`NodeTreeInterfaceSocketCollection.draw`](../N/bpy.types.NodeTreeInterfaceSocketCollection.md#bpy.types.NodeTreeInterfaceSocketCollection.draw "bpy.types.NodeTreeInterfaceSocketCollection.draw")
  * [`NodeTreeInterfaceSocketColor.draw`](../N/bpy.types.NodeTreeInterfaceSocketColor.md#bpy.types.NodeTreeInterfaceSocketColor.draw "bpy.types.NodeTreeInterfaceSocketColor.draw")
  * [`NodeTreeInterfaceSocketFloat.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloat.md#bpy.types.NodeTreeInterfaceSocketFloat.draw "bpy.types.NodeTreeInterfaceSocketFloat.draw")
  * [`NodeTreeInterfaceSocketFloatAngle.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatAngle.md#bpy.types.NodeTreeInterfaceSocketFloatAngle.draw "bpy.types.NodeTreeInterfaceSocketFloatAngle.draw")
  * [`NodeTreeInterfaceSocketFloatColorTemperature.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.md#bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.draw "bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.draw")
  * [`NodeTreeInterfaceSocketFloatDistance.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatDistance.md#bpy.types.NodeTreeInterfaceSocketFloatDistance.draw "bpy.types.NodeTreeInterfaceSocketFloatDistance.draw")
  * [`NodeTreeInterfaceSocketFloatFactor.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatFactor.md#bpy.types.NodeTreeInterfaceSocketFloatFactor.draw "bpy.types.NodeTreeInterfaceSocketFloatFactor.draw")
  * [`NodeTreeInterfaceSocketFloatFrequency.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatFrequency.md#bpy.types.NodeTreeInterfaceSocketFloatFrequency.draw "bpy.types.NodeTreeInterfaceSocketFloatFrequency.draw")
  * [`NodeTreeInterfaceSocketFloatPercentage.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatPercentage.md#bpy.types.NodeTreeInterfaceSocketFloatPercentage.draw "bpy.types.NodeTreeInterfaceSocketFloatPercentage.draw")
  * [`NodeTreeInterfaceSocketFloatTime.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatTime.md#bpy.types.NodeTreeInterfaceSocketFloatTime.draw "bpy.types.NodeTreeInterfaceSocketFloatTime.draw")
  * [`NodeTreeInterfaceSocketFloatTimeAbsolute.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.md#bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.draw "bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.draw")
  * [`NodeTreeInterfaceSocketFloatUnsigned.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatUnsigned.md#bpy.types.NodeTreeInterfaceSocketFloatUnsigned.draw "bpy.types.NodeTreeInterfaceSocketFloatUnsigned.draw")
  * [`NodeTreeInterfaceSocketFloatWavelength.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatWavelength.md#bpy.types.NodeTreeInterfaceSocketFloatWavelength.draw "bpy.types.NodeTreeInterfaceSocketFloatWavelength.draw")
  * [`NodeTreeInterfaceSocketGeometry.draw`](../N/bpy.types.NodeTreeInterfaceSocketGeometry.md#bpy.types.NodeTreeInterfaceSocketGeometry.draw "bpy.types.NodeTreeInterfaceSocketGeometry.draw")
  * [`NodeTreeInterfaceSocketImage.draw`](../N/bpy.types.NodeTreeInterfaceSocketImage.md#bpy.types.NodeTreeInterfaceSocketImage.draw "bpy.types.NodeTreeInterfaceSocketImage.draw")
  * [`NodeTreeInterfaceSocketInt.draw`](../N/bpy.types.NodeTreeInterfaceSocketInt.md#bpy.types.NodeTreeInterfaceSocketInt.draw "bpy.types.NodeTreeInterfaceSocketInt.draw")
  * [`NodeTreeInterfaceSocketIntFactor.draw`](../N/bpy.types.NodeTreeInterfaceSocketIntFactor.md#bpy.types.NodeTreeInterfaceSocketIntFactor.draw "bpy.types.NodeTreeInterfaceSocketIntFactor.draw")
  * [`NodeTreeInterfaceSocketIntPercentage.draw`](../N/bpy.types.NodeTreeInterfaceSocketIntPercentage.md#bpy.types.NodeTreeInterfaceSocketIntPercentage.draw "bpy.types.NodeTreeInterfaceSocketIntPercentage.draw")
  * [`NodeTreeInterfaceSocketIntUnsigned.draw`](../N/bpy.types.NodeTreeInterfaceSocketIntUnsigned.md#bpy.types.NodeTreeInterfaceSocketIntUnsigned.draw "bpy.types.NodeTreeInterfaceSocketIntUnsigned.draw")
  * [`NodeTreeInterfaceSocketMaterial.draw`](../N/bpy.types.NodeTreeInterfaceSocketMaterial.md#bpy.types.NodeTreeInterfaceSocketMaterial.draw "bpy.types.NodeTreeInterfaceSocketMaterial.draw")
  * [`NodeTreeInterfaceSocketMatrix.draw`](../N/bpy.types.NodeTreeInterfaceSocketMatrix.md#bpy.types.NodeTreeInterfaceSocketMatrix.draw "bpy.types.NodeTreeInterfaceSocketMatrix.draw")
  * [`NodeTreeInterfaceSocketMenu.draw`](../N/bpy.types.NodeTreeInterfaceSocketMenu.md#bpy.types.NodeTreeInterfaceSocketMenu.draw "bpy.types.NodeTreeInterfaceSocketMenu.draw")
  * [`NodeTreeInterfaceSocketObject.draw`](../N/bpy.types.NodeTreeInterfaceSocketObject.md#bpy.types.NodeTreeInterfaceSocketObject.draw "bpy.types.NodeTreeInterfaceSocketObject.draw")
  * [`NodeTreeInterfaceSocketRotation.draw`](../N/bpy.types.NodeTreeInterfaceSocketRotation.md#bpy.types.NodeTreeInterfaceSocketRotation.draw "bpy.types.NodeTreeInterfaceSocketRotation.draw")
  * [`NodeTreeInterfaceSocketShader.draw`](../N/bpy.types.NodeTreeInterfaceSocketShader.md#bpy.types.NodeTreeInterfaceSocketShader.draw "bpy.types.NodeTreeInterfaceSocketShader.draw")
  * [`NodeTreeInterfaceSocketString.draw`](../N/bpy.types.NodeTreeInterfaceSocketString.md#bpy.types.NodeTreeInterfaceSocketString.draw "bpy.types.NodeTreeInterfaceSocketString.draw")
  * [`NodeTreeInterfaceSocketStringFilePath.draw`](../N/bpy.types.NodeTreeInterfaceSocketStringFilePath.md#bpy.types.NodeTreeInterfaceSocketStringFilePath.draw "bpy.types.NodeTreeInterfaceSocketStringFilePath.draw")
  * [`NodeTreeInterfaceSocketTexture.draw`](../N/bpy.types.NodeTreeInterfaceSocketTexture.md#bpy.types.NodeTreeInterfaceSocketTexture.draw "bpy.types.NodeTreeInterfaceSocketTexture.draw")
  * [`NodeTreeInterfaceSocketVector.draw`](../N/bpy.types.NodeTreeInterfaceSocketVector.md#bpy.types.NodeTreeInterfaceSocketVector.draw "bpy.types.NodeTreeInterfaceSocketVector.draw")
  * [`NodeTreeInterfaceSocketVector2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVector2D.md#bpy.types.NodeTreeInterfaceSocketVector2D.draw "bpy.types.NodeTreeInterfaceSocketVector2D.draw")
  * [`NodeTreeInterfaceSocketVector4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVector4D.md#bpy.types.NodeTreeInterfaceSocketVector4D.draw "bpy.types.NodeTreeInterfaceSocketVector4D.draw")

| 

  * [`NodeTreeInterfaceSocketVectorAcceleration.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorAcceleration.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration.draw "bpy.types.NodeTreeInterfaceSocketVectorAcceleration.draw")
  * [`NodeTreeInterfaceSocketVectorAcceleration2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.draw "bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.draw")
  * [`NodeTreeInterfaceSocketVectorAcceleration4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.draw "bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.draw")
  * [`NodeTreeInterfaceSocketVectorDirection.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorDirection.md#bpy.types.NodeTreeInterfaceSocketVectorDirection.draw "bpy.types.NodeTreeInterfaceSocketVectorDirection.draw")
  * [`NodeTreeInterfaceSocketVectorDirection2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorDirection2D.md#bpy.types.NodeTreeInterfaceSocketVectorDirection2D.draw "bpy.types.NodeTreeInterfaceSocketVectorDirection2D.draw")
  * [`NodeTreeInterfaceSocketVectorDirection4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorDirection4D.md#bpy.types.NodeTreeInterfaceSocketVectorDirection4D.draw "bpy.types.NodeTreeInterfaceSocketVectorDirection4D.draw")
  * [`NodeTreeInterfaceSocketVectorEuler.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorEuler.md#bpy.types.NodeTreeInterfaceSocketVectorEuler.draw "bpy.types.NodeTreeInterfaceSocketVectorEuler.draw")
  * [`NodeTreeInterfaceSocketVectorEuler2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorEuler2D.md#bpy.types.NodeTreeInterfaceSocketVectorEuler2D.draw "bpy.types.NodeTreeInterfaceSocketVectorEuler2D.draw")
  * [`NodeTreeInterfaceSocketVectorEuler4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorEuler4D.md#bpy.types.NodeTreeInterfaceSocketVectorEuler4D.draw "bpy.types.NodeTreeInterfaceSocketVectorEuler4D.draw")
  * [`NodeTreeInterfaceSocketVectorFactor.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorFactor.md#bpy.types.NodeTreeInterfaceSocketVectorFactor.draw "bpy.types.NodeTreeInterfaceSocketVectorFactor.draw")
  * [`NodeTreeInterfaceSocketVectorFactor2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorFactor2D.md#bpy.types.NodeTreeInterfaceSocketVectorFactor2D.draw "bpy.types.NodeTreeInterfaceSocketVectorFactor2D.draw")
  * [`NodeTreeInterfaceSocketVectorFactor4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorFactor4D.md#bpy.types.NodeTreeInterfaceSocketVectorFactor4D.draw "bpy.types.NodeTreeInterfaceSocketVectorFactor4D.draw")
  * [`NodeTreeInterfaceSocketVectorPercentage.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorPercentage.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage.draw "bpy.types.NodeTreeInterfaceSocketVectorPercentage.draw")
  * [`NodeTreeInterfaceSocketVectorPercentage2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.draw "bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.draw")
  * [`NodeTreeInterfaceSocketVectorPercentage4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.draw "bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.draw")
  * [`NodeTreeInterfaceSocketVectorTranslation.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorTranslation.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation.draw "bpy.types.NodeTreeInterfaceSocketVectorTranslation.draw")
  * [`NodeTreeInterfaceSocketVectorTranslation2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.draw "bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.draw")
  * [`NodeTreeInterfaceSocketVectorTranslation4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.draw "bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.draw")
  * [`NodeTreeInterfaceSocketVectorVelocity.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorVelocity.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity.draw "bpy.types.NodeTreeInterfaceSocketVectorVelocity.draw")
  * [`NodeTreeInterfaceSocketVectorVelocity2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.draw "bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.draw")
  * [`NodeTreeInterfaceSocketVectorVelocity4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.draw "bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.draw")
  * [`NodeTreeInterfaceSocketVectorXYZ.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorXYZ.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ.draw "bpy.types.NodeTreeInterfaceSocketVectorXYZ.draw")
  * [`NodeTreeInterfaceSocketVectorXYZ2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.draw "bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.draw")
  * [`NodeTreeInterfaceSocketVectorXYZ4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.draw "bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.draw")
  * [`Operator.layout`](../O/bpy.types.Operator.md#bpy.types.Operator.layout "bpy.types.Operator.layout")
  * [`Panel.layout`](../P/bpy.types.Panel.md#bpy.types.Panel.layout "bpy.types.Panel.layout")
  * `UILayout.box`
  * `UILayout.column`
  * `UILayout.column_flow`
  * `UILayout.grid_flow`
  * `UILayout.menu_pie`
  * `UILayout.panel`
  * `UILayout.panel`
  * `UILayout.panel_prop`
  * `UILayout.panel_prop`
  * `UILayout.row`
  * `UILayout.split`
  * `UILayout.template_light_linking_collection`
  * [`UIList.draw_filter`](bpy.types.UIList.md#bpy.types.UIList.draw_filter "bpy.types.UIList.draw_filter")
  * [`UIList.draw_item`](bpy.types.UIList.md#bpy.types.UIList.draw_item "bpy.types.UIList.draw_item")
  * [`UIPieMenu.layout`](bpy.types.UIPieMenu.md#bpy.types.UIPieMenu.layout "bpy.types.UIPieMenu.layout")
  * [`UIPopover.layout`](bpy.types.UIPopover.md#bpy.types.UIPopover.layout "bpy.types.UIPopover.layout")
  * [`UIPopupMenu.layout`](bpy.types.UIPopupMenu.md#bpy.types.UIPopupMenu.layout "bpy.types.UIPopupMenu.layout")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
