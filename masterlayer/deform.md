# 🏔️ Deform

Displacement, World Position Offset, noise-driven deformation, animation, and wind systems.

---

### Displacement

| Parameter | Description |
|-----------|-------------|
| **Displacement Amount** | Threshold offset controlling how much of the height map drives displacement. |
| **Displacement Contrast** | Sharpens or softens the displacement distribution. |
| **Displacement** | The displacement color/height value used to offset surface geometry. Blue channel drives outward displacement by default. |

---

### ♦ use WPO

Enables World Position Offset for the layer.

| Parameter | Description |
|-----------|-------------|
| **VertexNormal - use Axis Direction** | Drives WPO along vertex normals instead of a fixed axis vector. |
| **WPO Strength** | Global WPO magnitude multiplier. |
| **WPO Offset** | Base directional offset applied before noise or animation layers. |

---

### ♦ use GrassWind

Activates SimpleGrassWind-based animation.

| Parameter | Description |
|-----------|-------------|
| **WPO WindIntensity** | Controls the amplitude of the wind-driven vertex displacement. |
| **WPO WindSpeed** | Controls the rate of the wind animation cycle. |
| **WPO WindWeight** | Blends wind influence across the mesh — typically painted via vertex color. |

---

### ♦ WPO Animation

Enables procedural time-driven animation of the WPO offset.

| Parameter | Description |
|-----------|-------------|
| **Periodic - Random Deform** | Switches between rhythmic sine-wave (OFF) and randomized (ON) deformation. |
| **WPO Speed** | Rate of the WPO animation cycle. |

---

### ♦ WPO Noise

Master toggle for WPO noise modulation.

| Parameter | Description |
|-----------|-------------|
| **WPO from CloudNoise** | Uses Unreal built-in cloud noise as the WPO noise source. |
| **WPO from Packed** | Reads noise data from a packed texture channel — saves a texture slot. |
| **WPO Noise Projection** | Projects the noise texture in world space — prevents UV-based stretching. |
| **WPO Noise Texture** | The texture asset driving the WPO noise pattern. |
| **WPO Noise Channel** | Selects the texture channel (R/G/B/A) carrying the noise data. |
| **WPO Noise Tiling** | UV scale for the noise texture. |
| **WPO Noise Amount** | Threshold offset controlling how much of the noise range drives displacement. |
| **WPO Noise Contrast** | Sharpens or softens the noise edges. |
