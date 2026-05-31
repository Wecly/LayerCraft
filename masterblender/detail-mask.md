# 🔍 Detail Mask

Secondary mask layered on top of the base mask — adds fine-detail variation and breakup. Supports attribute-specific masking and noise-driven detail.

---

| Parameter | Description |
|-----------|-------------|
| **use Detail Mask** | Enables the detail mask pass. |
| **Detail in Blend - use Overlay** | Routes the detail mask through the overlay system instead of the base blend. |
| **DetailMask Amount** | Threshold offset for the detail mask coverage. |
| **DetailMask Contrast** | Edge sharpness of the detail mask. |
| **Breakup Contrast** | Additional contrast applied to break up the detail mask edge for a more organic look. |

---

### Attribute Source

| Parameter | Description |
|-----------|-------------|
| **Detail Attribute - use Noise** | Switches the detail mask to noise-driven mode. |
| **from Bottom - use Top Layer** | Sources detail mask data from the bottom layer instead of the top. |
| **BaseColor** | Enables base color as a detail mask attribute source. |
| **Occlusion** | Enables occlusion as a detail mask attribute source. |
| **Roughness** | Enables roughness as a detail mask attribute source. |
| **Normal-B** | Enables normal map blue channel as a detail mask source. |
| **WPO** | Enables World Position Offset as a detail mask source. |
| **Displacement - use Opacity** | Uses displacement data as the detail mask, routed through opacity. |
| **BaseColor-Black** | Uses the dark regions of the base color as the mask. |
| **BaseColor Channel** | Selects which channel (R/G/B/A) of the base color texture drives the detail mask. |

---

### ♦ Detail Attribute - use Noise

Switches detail mask to noise-driven mode — a texture noise pattern drives the mask instead of attribute data.

| Parameter | Description |
|-----------|-------------|
| **Noise Texture - use Cloud Noise** | Uses Unreal built-in cloud noise as the detail noise source. |
| **Texture Noise - use Generated** | Uses procedurally generated noise instead of a texture asset. |
| **Noise Texture** | Texture asset driving the detail noise mask. |
| **Noise Channel** | Channel (R/G/B/A) of the noise texture used as the mask. |
| **Noise Tiling** | UV scale for the noise texture. |
| **Noise World Projection** | Projects noise in world space — prevents UV-based stretching. |
| **use Noise CustomCoords** | Enables custom UV channel for the noise texture. |
| **Noise Tiling X** | Horizontal UV scale for the noise. |
| **Noise Tiling Y** | Vertical UV scale for the noise. |
| **Noise Offset X** | Horizontal UV offset for the noise. |
| **Noise Offset Y** | Vertical UV offset for the noise. |
| **Noise Offset Z** | Z-axis UV offset for world-projected noise. |
| **use Noise Rotation** | Enables rotation of the noise UV. |
| **use NoiseAnimation** | Enables animated UV scrolling for the noise texture. |
| **NoiseAnimation Speed** | Scroll speed of the noise animation. |
| **NoiseAnimation Axis** | Direction vector for the noise animation. |
