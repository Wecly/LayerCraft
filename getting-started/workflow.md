# Workflow

**MaterialCraft** by default acts as a regular Master Material — parameters are in the Details tab and Layer Parameters tab will be None.

With **`use LayerCraft`** set to `True`, the system switches to Layer Parameters and is ready to accept the first Material Layer.

With a **Layer Asset** assigned, all Layer Parameters become active.

To switch back to MaterialCraft-only workflow, clear the Layer Asset and disable `use LayerCraft` from Details.

---

## System Assets

Main system assets can be found under `Materials/Masters`:

* Master Materials
* Master Layers
* Master Blenders

Besides the `use LayerCraft` bool, everything will be the same whether the material is used directly as MaterialCraft or as a layered workflow with LayerCraft. Parameters under **MaterialCraft** and **BakeCraft** are general post-layer processes that belong to both workflows.

---

## Your First Master Layer

LayerCraft is structured around a modular flow:

```
Layer  →  UV Logic  →  Textures  →  Color  →  Response  →  Detail  →  Deform  →  Variation
```

Everything needed to create any material lives under these Parameter Groups.
