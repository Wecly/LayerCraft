# How It Works

LayerCraft is built around two core assets that work together:

<img src="../images/ml-instance.png" style="max-width:100%; border-radius:6px; margin-bottom:12px;">

<img src="../images/mlb-instance.png" style="max-width:100%; border-radius:6px; margin-bottom:12px;">

<div style="display:flex; align-items:flex-start; gap:24px;">
<img src="../images/m-blend.png" style="width:320px; border-radius:6px;">
<p>You stack <code>ML_MasterLayer</code> instances in a material and control each transition with an <code>MLB_MasterBlender</code>. Every parameter is exposed, grouped, and documented in this reference.</p>
</div>

```
Layer  →  UV Logic  →  Textures  →  Color  →  Response  →  Detail  →  Deform  →  Variation
```
