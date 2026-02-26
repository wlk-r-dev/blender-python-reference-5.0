# Text(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.Text(_ID_)
    

Text data-block referencing an external or packed text file

current_character
    

Index of current character in current line, and also start index of character in selection if one exists

Type:
    

int in [0, inf], default 0

current_line
    

Current line, and start line of selection if one exists

Type:
    

[[TextLine]], (readonly, never None)

current_line_index
    

Index of current TextLine in TextLine collection

Type:
    

int in [-inf, inf], default 0

filepath
    

Filename of the text file

Type:
    

string, default “”, (never None)

indentation
    

Use tabs or spaces for indentation

  * `TABS` Tabs – Indent using tabs.

  * `SPACES` Spaces – Indent using spaces.


Type:
    

enum in [`'TABS'`, `'SPACES'`], default `'TABS'`

is_dirty
    

Text file has been edited since last save

Type:
    

boolean, default False, (readonly)

is_in_memory
    

Text file is in memory, without a corresponding file on disk

Type:
    

boolean, default False, (readonly)

is_modified
    

Text file on disk is different than the one in memory

Type:
    

boolean, default False, (readonly)

lines
    

Lines of text

Type:
    

[[bpy_prop_collection]] of [[TextLine]], (readonly)

select_end_character
    

Index of character after end of selection in the selection end line

Type:
    

int in [0, inf], default 0

select_end_line
    

End line of selection

Type:
    

[[TextLine]], (readonly, never None)

select_end_line_index
    

Index of last TextLine in selection

Type:
    

int in [-inf, inf], default 0

use_module
    

Run this text as a Python script on loading

Type:
    

boolean, default False

clear()
    

clear the text block

write(_text_)
    

write text at the cursor location and advance to the end of the text block

Parameters:
    

**text** (_string_ _,__(__never None_ _)_) – New text for this data-block

from_string(_text_)
    

Replace text with this string.

as_string()
    

Return the text as a string

Return type:
    

string, (never None)

is_syntax_highlight_supported()
    

Returns True if the editor supports syntax highlighting for the current text data-block

Return type:
    

boolean

select_set(_line_start_ , _char_start_ , _line_end_ , _char_end_)
    

Set selection range by line and character index

Parameters:
    

  * **line_start** (_int in_ _[__-inf_ _,__inf_ _]_) – Start Line

  * **char_start** (_int in_ _[__-inf_ _,__inf_ _]_) – Start Character

  * **line_end** (_int in_ _[__-inf_ _,__inf_ _]_) – End Line

  * **char_end** (_int in_ _[__-inf_ _,__inf_ _]_) – End Character


cursor_set(_line_ , _*_ , _character =0_, _select =False_)
    

Set cursor by line and (optionally) character index

Parameters:
    

  * **line** (_int in_ _[__0_ _,__inf_ _]_) – Line

  * **character** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Character

  * **select** (_boolean_ _,__(__optional_ _)_) – Select when moving the cursor


as_module()
    

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[[bpy.types.Struct]] subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

region_as_string(_*_ , _range =None_)
    

Parameters:
    

**range** (_tuple_ _[__tuple_ _[__int_ _,__int_ _]__,__tuple_ _[__int_ _,__int_ _]__]_) – The region of text to be returned, defaulting to the selection when no range is passed. Each int pair represents a line and column: ((start_line, start_column), (end_line, end_column)) The values match Python’s slicing logic (negative values count backwards from the end, the end value is not inclusive).

Returns:
    

The specified region as a string.

Return type:
    

str

region_from_string(_body_ , _/_ , _*_ , _range =None_)
    

Parameters:
    

  * **body** (_str_) – The text to be inserted.

  * **range** (_tuple_ _[__tuple_ _[__int_ _,__int_ _]__,__tuple_ _[__int_ _,__int_ _]__]_) – The region of text to be returned, defaulting to the selection when no range is passed. Each int pair represents a line and column: ((start_line, start_column), (end_line, end_column)) The values match Python’s slicing logic (negative values count backwards from the end, the end value is not inclusive).


## Inherited Properties

  * [[bpy_struct.id_data]]
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]

| 

  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]

  
---|---  
  
## Inherited Functions

  * [[bpy_struct.as_pointer]]
  * [[bpy_struct.driver_add]]
  * [[bpy_struct.driver_remove]]
  * [[bpy_struct.get]]
  * [[bpy_struct.id_properties_clear]]
  * [[bpy_struct.id_properties_ensure]]
  * [[bpy_struct.id_properties_ui]]
  * [[bpy_struct.is_property_hidden]]
  * [[bpy_struct.is_property_overridable_library]]
  * [[bpy_struct.is_property_readonly]]
  * [[bpy_struct.is_property_set]]
  * [[bpy_struct.items]]
  * [[bpy_struct.keyframe_delete]]
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]

| 

  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[bpy.context.edit_text]]
  * [[BlendData.texts]]
  * [[BlendDataTexts.load]]
  * [[BlendDataTexts.new]]
  * [[BlendDataTexts.remove]]
  * [[Camera.custom_shader]]

| 

  * [[FreestyleModuleSettings.script]]
  * [[NodeFrame.text]]
  * [[ShaderNodeScript.script]]
  * [[ShaderNodeTexIES.ies]]
  * [[SpaceTextEditor.text]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
