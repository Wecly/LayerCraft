# 🎭 Base Mask

Defines the primary mask driving layer visibility. Supports anchor masks, procedural generation, and texture-based masking — combinable for complex blending setups.

<img src="images/image50.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

---

### Anchor Mask

| Parameter | Description |
|-----------|-------------|
| **use AnchorMask** | Uses a baked anchor mask as the blend base — locks coverage from a previously saved mask pass. |
| **AnchorMask Amount** | Threshold offset for the anchor mask. |
| **AnchorMask Contrast** | Edge sharpness of the anchor mask. |
| **use 2nd Base Mask** | Enables a second base mask combined with the primary. |

---

### ♦ use Base Mask Controls

Reveals additional mask controls: amount, contrast, range, and invert.

<img src="images/image60.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **BaseMask Amount** | Global threshold offset for the final mask output. |
| **BaseMask Contrast** | Edge sharpness of the final mask. |
| **use Base Mask in Range** | Clamps the mask output to a defined range. |
| **BaseMask Range** | Maximum range value when `Use Base Mask in Range` is active. |

---

### ♦ use Procedural Mask

<img src="images/image9.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

Enables procedurally generated masking. Exposes multiple mask types:

| Type | Description |
|------|-------------|
| **Gradient** | Linear gradient mask in world or object space. |
| **Directional** | Surface angle mask — driven by normal facing direction. |
| **EdgeWear** | Curvature-based edge wear mask — concentrates blend on high-curvature edges. |
| **UV** | UV coordinate-based procedural mask. |
| **Distance** | Distance-from-point or actor proximity mask. |
| **RVT** | Runtime Virtual Texture-sourced mask. |
| **Actor** | Actor proximity-based mask. |
| **Light** | Scene light-driven mask. |

> **use 2nd Procedural Mask** — Adds a second independent procedural mask combined with the first.

---

### ♦ use Texture Mask

Enables a texture asset as the primary blend mask.

<img src="images/image44.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **TextureMask Amount** | Threshold offset shifting mask coverage. |
| **TextureMask Contrast** | Edge sharpness of the mask. |
| **Texture - use Cloud Mask** | Uses Unreal built-in cloud noise instead of a custom texture. |
| **TextureMask** | The texture asset driving the mask. |
| **TextureMask Sampler: Clamped?** | Clamp sampler — disables texture repeat. |
| **TextureMask Channel** | Channel (R/G/B/A) used as the mask. |
| **TextureMask Tiling** | Uniform UV scale for the mask texture. |
| **use TextureMask Rotation** | Enables UV rotation for the mask texture. |
| **TextureMask Rotation** | Rotation angle for the mask UV in degrees. |
| **TextureMask World Projection** | Projects mask in world space — prevents UV stretching. |
| **use TextureMask Animation** | Enables animated UV scrolling for the mask texture. |
| **TextureMaskAnimation Speed** | Scroll speed of the mask animation. |
| **TextureMaskAnimation Axis** | Direction vector for the mask UV animation. |

#### use TextureMask Tiling Controls

<img src="images/image43.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **TextureMask Tiling X** | Horizontal UV scale for the mask texture. |
| **TextureMask Tiling Y** | Vertical UV scale for the mask texture. |
| **TextureMask Tiling Z** | Z-axis UV scale for world-projected masks. |
| **TextureMask Offset X** | Horizontal UV offset. |
| **TextureMask Offset Y** | Vertical UV offset. |
| **TextureMask Offset Z** | Z-axis UV offset for world-projected masks. |

<img src="images/image65.jpg" style="max-width:100%; border-radius:6px; margin-top:16px;">
<img src="images/image10.jpg" style="max-width:100%; border-radius:6px; margin-top:8px;">
