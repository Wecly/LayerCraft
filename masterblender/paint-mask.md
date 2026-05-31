# 🎨 Paint Mask

Artist-driven mask using vertex color or a painted texture — gives direct control over layer placement without procedural rules.

<img src="images/image47.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

---

| Parameter | Description |
|-----------|-------------|
| **use Paint Mask** | Enables the paint mask pass. |
| **Vertex - use TexturePaint** | Switches between vertex color paint (OFF) and texture paint (ON). |
| **Blend - use Paint as Base Mask** | Uses the paint mask as the primary base mask instead of an additive detail pass. |
| **Erase - Overlay Paint** | Inverts the paint mask behavior — painted areas erase the layer instead of revealing it. |
| **PaintMask Channel** | Selects the vertex color or texture channel (R/G/B/A) used as the paint mask. |
| **PaintMask Amount** | Threshold offset for the paint mask coverage. |
| **PaintMask Contrast** | Edge sharpness of the paint mask. |
| **use Paint in Range** | Clamps the paint mask to a defined range. |
