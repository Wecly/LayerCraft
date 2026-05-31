# MLB\_MasterBlender

**Blend Asset Reference**

`MLB_MasterBlender` controls how two material layers are composited together. It manages blend behavior, base masking, detail masking, paint data, and overlay compositing through five parameter groups.

| Group | Description |
|-------|-------------|
| **BLEND** | Blend method, per-attribute weights, debug, parallax shadow, and anchor mask. |
| **BASEMASK** | Primary mask — anchor, procedural, and texture mask modes. |
| **DETAIL MASK** | Secondary mask for fine-detail variation. |
| **PAINT MASK** | Vertex or texture paint mask for artist-driven layer placement. |
| **OVERLAY** | Final compositing pass — per-layer color, roughness, and normal variation. |
