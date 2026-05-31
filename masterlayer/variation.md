# 🎲 Variation

Noise overlay and per-instance randomization systems for color, roughness, normals, and displacement.

---

### ♦ use Noise Overlay

Enables a texture-driven noise overlay that modulates color, roughness, displacement, and normals across the surface.

| Parameter | Description |
|-----------|-------------|
| **Noise Texture - use Cloud Noise** | Uses cloud noise as the variation source instead of a custom texture. |
| **use Noise Variation World Projection** | Projects the noise in world space — prevents UV-based stretching. |
| **Noise Tiling** | Uniform UV scale for the noise texture. |
| **Noise Tiling X** | Independent horizontal UV scale for the noise texture. |
| **Noise Texture** | The texture asset driving the variation noise. |

---

### ♦ use Noise Color

Enables noise-driven color variation.

| Parameter | Description |
|-----------|-------------|
| **Noise Color** | The color tint applied in noise-bright regions. |
| **Noise Color Channel** | Selects the texture channel (R/G/B/A) driving color variation. |
| **Noise Color Amount** | Threshold offset for the color noise mask. |
| **Noise Color Contrast** | Edge sharpness of the color variation mask. |

---

### ♦ use Noise Roughness

Enables noise-driven roughness variation — adds surface-level roughness detail independent of the base ORM.

| Parameter | Description |
|-----------|-------------|
| **Noise Roughness Channel** | Selects the texture channel driving roughness variation. |
| **Noise Roughness Amount** | Threshold offset for the roughness noise mask. |
| **Noise Roughness Contrast** | Edge sharpness of the roughness variation mask. |

---

### ♦ use Noise Displacement

Enables noise-driven displacement variation — adds localized height offset on top of the base displacement.

| Parameter | Description |
|-----------|-------------|
| **Noise Displacement Channel** | Selects the texture channel driving displacement variation. |
| **Noise Displacement Amount** | Threshold offset for the displacement noise mask. |
| **Noise Displacement Contrast** | Edge sharpness of the displacement variation mask. |

---

### ♦ use Noise Normal

Enables noise-driven normal intensity variation — locally strengthens or weakens surface detail based on the noise mask.

| Parameter | Description |
|-----------|-------------|
| **Noise Normal Intensity** | Multiplier for normal map strength within noise-affected regions. |
| **Noise Normal Channel** | Selects the texture channel driving normal variation. |
| **Noise Normal Amount** | Threshold offset for the normal noise mask. |
| **Noise Normal Contrast** | Edge sharpness of the normal variation mask. |

---

### ♦ use Randomization

Enables per-instance randomization of color, roughness, normals, and displacement.

| Parameter | Description |
|-----------|-------------|
| **Random Rate** | Controls the rate of randomization across instances. |

#### use Random Color

| Parameter | Description |
|-----------|-------------|
| **Color - use Random HueShift** | Switches random color mode from direct tint to hue rotation. |
| **Random Brightness Amount** | Range of random brightness variation per instance. |
| **Random Desaturation Amount** | Range of random desaturation per instance. |
| **RandomColor1** | First color in the random color palette. |
| **RandomColor2** | Second color in the random color palette. |
| **use Random 2Color** | Enables dual-color random interpolation. |

#### use Random Roughness

| Parameter | Description |
|-----------|-------------|
| **Random Roughness Amount** | Range of roughness variation applied per instance. |

#### use Random Normal

| Parameter | Description |
|-----------|-------------|
| **Random Normal Intensity** | Range of normal map strength variation per instance. |

#### use Random Displacement

| Parameter | Description |
|-----------|-------------|
| **Random Displacement Amount** | Range of displacement variation per instance. |
