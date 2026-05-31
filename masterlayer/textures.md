# 🖼️ Textures

All the texture inputs and packing methods are set here.

<img src="images/image6.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

---

### Texture Slots

| Parameter | Description |
|-----------|-------------|
| **use Albedo Texture** | Enables the Albedo texture input slot. |
| **use Packed Texture** | Enables the Packed texture input — routes ORM or other packed data. |
| **use Normal Texture** | Enables the Normal map texture input slot. |
| **use Packed Normal** | Enables the PackedNormal texture — extracts normals from R and G channels. |
| **use Displacement Texture** | Enables a dedicated Displacement texture input separate from the packed channel. |
| **use Sampler Clamped** | Changes the sampler to Clamp mode — disables tiling repeat. Required for decals, atlas trimsheets, and unique surfaces. |

---

### ♦ use Texture Array

Switches texture inputs to Texture 2D Array mode — enables index-based or randomized selection from an array asset.

<img src="images/image70.jpg" style="max-width:100%; border-radius:6px; margin-bottom:8px;">
<img src="images/image5.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **use Texture Array Random Index** | Assigns a random array index per instance — produces automatic texture variation. |
| **Texture Array Index** | Fixed index into the texture array. |
| **Albedo Texture Array** | Texture 2D Array asset for the albedo channel. |
| **Packed Texture Array** | Texture 2D Array asset for the packed ORM/data channel. |
| **Normal Texture Array** | Texture 2D Array asset for the normal map channel. |
| **Texture Array Size** | Total number of slices in the Texture 2D Array. Required for correct random index calculation. |

> **How to create a Texture 2D Array:** Content Browser > Create Advanced Asset > Texture > Texture 2D Array, then populate its Source Textures array with your texture assets.

<img src="images/image67.jpg" style="max-width:100%; border-radius:6px; margin-bottom:8px;">
<img src="images/image30.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

---

### ♦ use Virtual Textures

Switches all texture inputs to Virtual Texture counterparts — enables RVT streaming workflow.

<img src="images/image18.jpg" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **Albedo V-Texture** | Virtual Texture asset for the albedo channel. |
| **Packed V-Texture** | Virtual Texture asset for the packed data channel. |
| **Normal V-Texture** | Virtual Texture asset for the normal map channel. |
| **use Sampler Clamped** | Clamp sampler — disables UV repeat. Required for unique-mapped or atlas-based surfaces. |

<img src="images/image8.jpg" style="max-width:100%; border-radius:6px; margin-top:16px;">
