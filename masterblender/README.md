# MLB\_MasterBlender

**Blend Asset Reference**

<div style="display:flex; align-items:flex-start; gap:40px;">

<img src="images/mlb-asset-groups.png" style="width:260px; border-radius:6px;">

<div>

`MLB_MasterBlender` controls how two material layers are composited together. It manages blend behavior, base masking, detail masking, paint data, and overlay compositing through five parameter groups.

</div>
</div>

---

| Group | Description |
|-------|-------------|
| **BLEND** | Blend method, per-attribute weights, debug, parallax shadow, and anchor mask. |
| **BASEMASK** | Primary mask — anchor, procedural, and texture mask modes. |
| **DETAIL MASK** | Secondary mask for fine-detail variation. |
| **PAINT MASK** | Vertex or texture paint mask for artist-driven layer placement. |
| **OVERLAY** | Final compositing pass — per-layer color, roughness, and normal variation. |
