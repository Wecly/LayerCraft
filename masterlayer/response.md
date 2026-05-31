# 💎 Response

Controls all PBR response attributes — Roughness, Specular, Metallic, and Opacity.

<img src="images/image64.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

---

### Base Response

| Parameter | Description |
|-----------|-------------|
| **use Specular from Albedo** | Derives specular intensity directly from the albedo texture. |
| **use Specular from Roughness** | Derives specular intensity from the roughness output — smoother areas receive stronger specular. |
| **Roughness** | Selects the texture channel used as the roughness source. Green channel is standard for packed ORM. |
| **Roughness Amount** | Threshold offset shifting the roughness value across the surface. |
| **Roughness Contrast** | Controls the spread of roughness values. Higher contrast pushes toward fully rough or fully smooth. |
| **Specular Amount** | Base specular intensity multiplier. `0.5` is the PBR default for dielectric surfaces. |

---

### ♦ use Metallic

Enables metallic workflow controls. Exposes channel selection and amount for per-layer metallic masking.

---

### ♦ use Opacity

Enables the opacity/transparency system. Exposes mask, fade, amount, and texture controls.

| Parameter | Description |
|-----------|-------------|
| **Opacity Mask - use Overall** | Uses a global opacity mask that applies across the entire layer. |
| **Opacity Mask Dither** | Enables dithered transparency — creates a screen-door dissolve pattern. |

<img src="images/image38.jpg" style="max-width:100%; border-radius:6px; margin-top:16px;">
| **PerInstanceFade** | Amount ready to be integrated for foliage optimization. |
| **Opacity Amount** | Base opacity threshold. `1.0` = fully opaque. |
| **Opacity Contrast** | Controls how abruptly the surface transitions from opaque to transparent. |
| **use Opacity from Albedo** | Sources opacity data from a packed channel of the albedo texture. |

<img src="images/image23.png" style="max-width:100%; border-radius:6px; margin-top:16px;">
| **Alpha - use Black Mask** | Uses black values of Albedo as Opacity Mask instead of Alpha channel. |
| **Packed - use Opacity Texture** | Sources opacity data from dedicated Opacity Texture instead of Packed Texture. |
