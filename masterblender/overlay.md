# ✨ Overlay

Final compositing pass applied on top of all blend operations. Adds per-layer color, roughness, and normal variation driven by the blend mask — each layer gets independent overlay attributes.

---

| Parameter | Description |
|-----------|-------------|
| **use Overlay** | Enables the overlay compositing pass. |
| **Overlay Layers - use Blend** | Routes overlay through the blend mask — overlay intensity is modulated by the base mask. |
| **Overlay Bottom Amount** | Threshold offset for the overlay on the bottom layer. |
| **Overlay Bottom Contrast** | Edge sharpness of the bottom layer overlay mask. |
| **Overlay Top Amount** | Threshold offset for the overlay on the top layer. |
| **Overlay Top Contrast** | Edge sharpness of the top layer overlay mask. |

---

### ♦ Overlay BaseColor

Enables base color overlay — applies tint, desaturation, and brightness independently per layer.

| Parameter | Description |
|-----------|-------------|
| **Overlay BaseColor perLayer - use Both** | Applies overlay base color to both layers simultaneously. |
| **Overlay Bottom Desaturation** | Desaturation applied to the bottom layer via overlay. |
| **Overlay Bottom Brightness** | Brightness adjustment for the bottom layer via overlay. |
| **Overlay Bottom Tint** | Color tint applied to the bottom layer via overlay. |
| **Overlay Top Desaturation** | Desaturation applied to the top layer via overlay. |
| **Overlay Top Brightness** | Brightness adjustment for the top layer via overlay. |
| **Overlay Top Tint** | Color tint applied to the top layer via overlay. |

---

### ♦ Overlay Roughness

Enables roughness variation via overlay — adjusts roughness per layer independently.

---

### ♦ Overlay Normal

Enables normal variation and edge-based normal generation via overlay.

| Parameter | Description |
|-----------|-------------|
| **Normal Edge Blend** | Generates normals from the blend mask edge — creates a raised or recessed edge normal at layer boundaries. |
| **Edge Normal Intensity** | Strength of the edge-generated normal. |
| **Edge Normal Curve** | Controls the curvature profile of the edge normal. |

#### use Overlay Detail Normal

Adds a detail normal texture on top of the overlay normal pass.

| Parameter | Description |
|-----------|-------------|
| **Overlay Detail Normal Bottom - use Top** | Applies the overlay detail normal to the bottom layer instead of the top. |
| **Detail Normal Intensity** | Blend strength of the overlay detail normal. |
| **Overlay Detail Normal Texture** | Texture asset for the overlay detail normal pass. |
| **Detail Normal Tiling** | UV scale for the overlay detail normal texture. |
