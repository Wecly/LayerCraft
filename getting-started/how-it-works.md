# How It Works

LayerCraft is built around two core assets that work together:

* **ML\_MasterLayer** — a Material Layer defining how a single surface looks: its textures, UVs, color, response, detail normals, deformation, and variation.
* **MLB\_MasterBlender** — a Material Layer Blend that controls how two layers are composited together: which channels blend, how masking works, and how the blend transitions between layers.

You stack `ML_MasterLayer` instances in a material and control each transition with an `MLB_MasterBlender`. Every parameter is exposed, grouped, and documented in this reference.

```
Layer  →  UV Logic  →  Textures  →  Color  →  Response  →  Detail  →  Deform  →  Variation
```
