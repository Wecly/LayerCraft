# 🎭 Layer

What kind of layer it will be? Here you can control the material attributes creation and control some general features.

<img src="images/image32.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

---

| Parameter | Description |
|-----------|-------------|
| **Debug** | Visualizes individual material attributes in the viewport — Roughness, AO, Normal, Displacement, WPO Noise, Noise Overlay. For diagnostics only, disable before rendering. |
| **use None** | Outputs a blank/transparent layer. Useful as a placeholder slot when building multi-layer stacks. |

---

### ♦ use RVT Layer

Switches the layer input to a Runtime Virtual Texture — reads color, normal, and height from a baked RVT.

<img src="images/image57.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **use RVT Projection** | Applies world-space UV projection to the RVT read — eliminates UV stretching on non-flat surfaces. |
| **RVT-Disp Texture** | Runtime Virtual Texture asset providing displacement data. |
| **RVT-Mat Texture** | Runtime Virtual Texture asset providing color, roughness, and material attribute data. |
| **RVT-Height Texture** | Runtime Virtual Texture asset providing height data used for displacement and POM. |

---

### ♦ use Raw Layer

Enables a texture-free constant material mode. All surface values are set directly as numeric constants.

<img src="images/image16.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **Raw Color** | Flat constant color applied across the entire surface. |
| **Raw Metallic** | Constant metallic value. `0.0` = dielectric, `1.0` = fully metallic. |
| **Raw Specular** | Constant specular intensity. `0.5` is the PBR default. |
| **Raw Roughness** | Constant roughness value. `0.0` = mirror-smooth, `1.0` = fully diffuse. |

---

### ♦ Material - use Attributes

Switches to per-channel attribute routing — lets you enable or disable each material output independently.

<img src="images/image54.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **use BaseColor** | Enables the Base Color channel output. |
| **use EmissiveColor** | Enables the Emissive Color channel output. |
| **use Roughness** | Enables the Roughness channel output. |
| **use Specular** | Enables the Specular channel output. |
| **use Metallic** | Enables the Metallic channel output. |
| **use Occlusion** | Enables the Ambient Occlusion channel output. |
| **use Normal** | Enables the Normal map channel output. |
| **use Displacement** | Enables the Displacement channel output. |
| **use WorldPositionOffset** | Enables the World Position Offset channel output. |
| **use Opacity** | Enables the Opacity channel output. |

---

### ♦ use Texture Sets

Selects a predefined packed texture format — automatically routes the correct channels without manual setup.

<img src="images/image29.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Value | Description |
|-------|-------------|
| **NDp** | Normal.X (R) + Normal.Y (G) + Displacement (B) |
| **NRDp** | Normal.X (R) + Normal.Y (G) + Roughness (B) + Displacement (A) |
| **ORDp** | Occlusion (R) + Roughness (G) + Displacement (B) |
| **ORM + Dp** | Occlusion (R) + Roughness (G) + Metallic (B) + separate NDp for displacement |
| **ORM - use ORMDp** | Occlusion (R) + Roughness (G) + Metallic (B) + Displacement (A) — all four in one texture |

---

### ♦ use CPD-Color

Exposes color parameters to Custom Primitive Data — enables per-instance color override set in Details > Rendering > CPD.

<img src="images/image2.jpg" style="max-width:100%; border-radius:6px; margin-bottom:8px;">
<img src="images/image36.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **CPD/0 use CPD/1** | Selects which CPD slot (0 or 1) drives the parameter. |
| **CPD/0 - Mask Amount** | Index 0 — drives the layer mask threshold for the first CPD layer. |
| **CPD/1 - Mask Amount** | Index 1 — drives the layer mask threshold for the second CPD layer. |
| **CPD/0 - UV Tiling - X** | Index 2 — drives horizontal UV tiling for the first CPD layer. |
| **CPD/1 - UV Tiling - X** | Index 3 — drives horizontal UV tiling for the second CPD layer. |
| **CPD/0 - UV Tiling - Y** | Index 4 — drives vertical UV tiling for the first CPD layer. |
| **CPD/1 - UV Tiling - Y** | Index 5 — drives vertical UV tiling for the second CPD layer. |
| **CPD/0 - UV Offset - X** | Index 6 — drives horizontal UV offset for the first CPD layer. |
| **CPD/1 - UV Offset - X** | Index 7 — drives horizontal UV offset for the second CPD layer. |
| **CPD/0 - UV Offset - Y** | Index 8 — drives vertical UV offset for the first CPD layer. |
| **CPD/1 - UV Offset - Y** | Index 9 — drives vertical UV offset for the second CPD layer. |
| **CPD/0 - Color Desaturation** | Index 10 — drives color desaturation for the first CPD layer. |
| **CPD/1 - Color Desaturation** | Index 11 — drives color desaturation for the second CPD layer. |
| **CPD/0 - Color HueShift** | Index 12 — drives hue rotation for the first CPD layer. |
| **CPD/1 - Color HueShift** | Index 13 — drives hue rotation for the second CPD layer. |
| **CPD/0 - Color Brightness** | Index 14 — drives brightness for the first CPD layer. |
| **CPD/1 - Color Brightness** | Index 15 — drives brightness for the second CPD layer. |
| **CPD/0 - Array Index** | Index 16 — drives the Texture Array index for the first CPD layer. |
| **CPD/1 - Array Index** | Index 17 — drives the Texture Array index for the second CPD layer. |
