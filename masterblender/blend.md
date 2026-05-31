# ⚙️ Blend

Blend group controls how layers are combined. Use Parallax Shadow to carry the bottom layer shadow through to the top, creating realistic contact depth at layer boundaries.

<img src="images/image34.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

---

### Debug Tools

| Parameter | Description |
|-----------|-------------|
| **Debug Overlay Mask** | Shows the overlay mask contribution in isolation. |
| **Debug Blend - use Base Mask** | Displays the base mask driving the blend. |
| **Debug Color** | Fills the surface with a solid debug color for mask coverage inspection. |
| **Debug Gamma Correction** | Applies gamma correction to the debug view for accurate brightness representation. |
| **Save Anchor Mask** | Bakes the current mask state as an anchor — locks blend coverage for subsequent passes. |

---

### ♦ use Parallax Shadow

Applies a parallax-based contact shadow at the layer boundary — carries the bottom layer shadow onto the top layer for realistic depth.

<img src="images/image11.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

---

### ♦ Material - use Attribute Blend

Switches to per-attribute blending — each material channel can be blended independently.

<img src="images/image31.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **use Attribute Weights** | Enables independent weight multipliers per channel. |
| **use Material from Bottom Layer** | Sources all material attributes from the layer below. |
| **BaseColor Weight** | Blend weight for the base color channel. `1.0` = this layer, `0.0` = layer below. |
| **use Normal Blend** | Activates dedicated normal map blending. |
| **Normal Weight** | Blend weight for the normal channel. |
| **Roughness Weight** | Blend weight for the roughness channel. |
| **WPO Weight** | Blend weight for the World Position Offset channel. |
| **Occlusion Weight** | Blend weight for the occlusion channel. |
| **Opacity Weight** | Blend weight for the opacity channel. |
| **Specular Weight** | Blend weight for the specular channel. |
| **Metallic Weight** | Blend weight for the metallic channel. |
| **Displacement Weight** | Blend weight for the displacement channel. |
| **Emissive Weight** | Blend weight for the emissive channel. |

Independent toggles: **use BaseColor**, **use Emissive**, **use Roughness**, **use Metallic**, **use Normal**, **use Displacement**, **use Specular**, **use WPO**, **use Occlusion**, **use Opacity**

<img src="images/image4.jpg" style="max-width:100%; border-radius:6px; margin-top:16px;">
<img src="images/image17.jpg" style="max-width:100%; border-radius:6px; margin-top:8px;">
