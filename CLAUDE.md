# Blender 5.0 Python API Reference

> **⚠️ This repo is READ-ONLY reference material.** Do not commit generated code, scripts, or project files here. Use this solely as a lookup resource when building bpy tools.

Markdown documentation (converted from HTML) for `bpy` — Blender's Python API (version 5.0). Use this to look up classes, operators, properties, and types when building Blender scripts, addons, or automation tools.

## File Structure

Files are organized into subfolders by module. Root contains core entry points and indexes.

### Root Files
| File | What It Covers |
|---|---|
| `bpy.context.md` | **Context** — active object, selected objects, mode, scene |
| `bpy.data.md` | **Data access** — `bpy.data.objects`, `.meshes`, `.materials`, etc. |
| `bpy.props.md` | **Properties** — IntProperty, FloatProperty, etc. for addons |
| `bpy.path.md` | **Path utilities** — Blender-specific path helpers |
| `bpy.msgbus.md` | **Message bus** — subscribe to property changes |
| `mathutils.md` | **Math** — Vector, Matrix, Quaternion, Euler |
| `aud.md` | **Audio** — sound playback |
| `blf.md` | **Font** — text drawing in the viewport |
| `bgl.md` | **OpenGL** — direct GL calls (deprecated, prefer `gpu`) |
| `bl_math.md` | **Math helpers** — clamp, lerp, smoothstep |
| `idprop.types.md` | **ID Properties** — custom data on any datablock |
| `index.md` | Main landing page |
| `py-modindex.md` | Module index |
| `search.md` | Built-in search (browser) |

### Subfolders
| Folder | Contents | Files |
|---|---|---|
| `bpy.types/A-Z/` | **Types** — RNA types, nodes, modifiers, constraints. Split by first letter. | ~1670 |
| `bpy.types/_other/` | Base types (`bpy_struct`, `bpy_prop_collection`, `wm*`) | 6 |
| `bpy.ops/` | **Operators** — all `bpy.ops.*` modules | 78 |
| `bpy.app/` | **App info** — handlers, timers, translations, version info | 5 |
| `bpy.utils/` | **Utilities** — register/unregister, previews, script paths | 3 |
| `bpy_extras/` | **Extras** — anim, asset, io, mesh, object, view3d utils | 11 |
| `bmesh/` | **BMesh** — low-level mesh editing (verts, edges, faces, ops) | 5 |
| `mathutils/` | **Math submodules** — bvhtree, geometry, interpolate, kdtree, noise | 5 |
| `gpu/` | **GPU module** — modern shader/draw API | 9 |
| `gpu_extras/` | **GPU extras** — batch, presets | 3 |
| `freestyle/` | **Freestyle** — non-photorealistic line rendering | 8 |
| `imbuf/` | **Image buffer** — image types | 2 |
| `info/` | **Guides** — quickstart, gotchas, best practices, tips | 15 |
| `bpy_types_enum_items/` | Enum item reference pages | ~199 |
| `_static/` | CSS, JS, images for the docs | ~32 |

### Finding a Type
To find `bpy.types.Mesh`, look in `bpy.types/M/bpy.types.Mesh.md` (first letter of the type name).

### Finding an Operator
To find `bpy.ops.mesh.*`, look in `bpy.ops/bpy.ops.mesh.md`.

## How to Troubleshoot

### "AttributeError: 'X' has no attribute 'Y'"
1. Open `bpy.types.X.md` and check the actual property/method names
2. Properties may have been renamed or moved between versions

### "RuntimeError: Operator bpy.ops.X.Y.poll() failed"
1. Open `bpy.ops.X.md`, find operator `Y`
2. Check the **poll** conditions — usually requires correct mode/context
3. Common fix: ensure correct `bpy.context.area.type` or object mode

### "Context is incorrect"
1. Check `bpy.context.md` for what's available in your context
2. Operators often need specific area types — use `bpy.ops.X.Y('INVOKE_DEFAULT')` vs `('EXEC_DEFAULT')`
3. Override context with `with bpy.context.temp_override(...):`

### Finding the right operator
1. In Blender: hover over any button → status bar shows `bpy.ops.*` call
2. Or search `bpy.ops.md` for the index of all operator modules
3. Then open the specific `bpy.ops.<module>.md` for full signatures

### Finding the right type/property
1. Start at `bpy.types.Object.md` for object-level properties
2. Follow links to specific types: `Mesh.md`, `Material.md`, etc.
3. `bpy.types.bpy_struct.md` is the base class for all RNA types

## Common Workflows

### Mesh manipulation
- High-level: `bpy.ops.mesh.*` (requires edit mode)
- Low-level: `bmesh` module (create BMesh from mesh data, edit, write back)
- Read `bmesh.md` → `bmesh.types.md` → `bmesh.ops.md`

### Materials & Shaders
- `bpy.types.Material.md` → material settings
- `bpy.types.ShaderNode*.md` → all shader node types
- `bpy.types.ShaderNodeTree.md` → node tree management

### Modifiers
- `bpy.types.*Modifier.md` — one file per modifier type
- Add via `obj.modifiers.new(name, type)` — types listed in `bpy.types.Modifier.md`

### Geometry Nodes
- `bpy.types.GeometryNode*.md` — all geometry node types
- `bpy.types.GeometryNodeTree.md` — the node tree itself
- `bpy.types.NodesModifier.md` — the modifier that applies a node group

### Import/Export
- `bpy.ops.import_scene.md` / `bpy.ops.export_scene.md`
- `bpy.ops.import_anim.md` / `bpy.ops.export_anim.md`

### Handlers & Automation
- `bpy.app.handlers.md` — run code on file load, frame change, render, etc.
- `bpy.app.timers.md` — periodic callbacks
- `bpy.msgbus.md` — subscribe to property changes

## Tips

- **Always check the version** — this is 5.0. APIs change between versions.
- **RNA vs Python** — most properties are RNA (defined in C). Custom ones use `bpy.props`.
- **`bpy.types.md`** has the full alphabetical index of all types.
- **`py-modindex.md`** has the module index.
- **`searchindex.js`** + **`search.md`** — built-in search if viewed in a browser.
