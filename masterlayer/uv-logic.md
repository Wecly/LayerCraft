# 🗺️ UV Logic

All math logic for UV mapping the textures. From projection to fake displacement, variations to animations — almost all UV logic is handled here.

<img src="images/image73.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

---

### Base UV

| Parameter | Description |
|-----------|-------------|
| **Tiling** | Global uniform UV scale for all textures in the layer. Higher values tile the texture more densely. |

---

### ♦ use Tiling Controls

Reveals per-axis tiling, offset, and rotation controls — replaces the single Tiling value with full UV transform options.

<img src="images/image25.png" style="max-width:100%; border-radius:6px; margin-bottom:8px;">
<img src="images/image26.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **use CustomCoords** | Enables custom UV channel selection — allows routing a specific mesh UV channel instead of the default UV0. |
| **UV Coord Index** | Index of the mesh UV channel to use when Custom Coords is active. |
| **Tiling X** | Horizontal UV scale independent of vertical. |
| **Tiling Y** | Vertical UV scale independent of horizontal. |
| **Tiling Z** | Z-axis UV scale — applies to world-projection or triplanar Z face. |
| **Offset X** | Horizontal UV offset — shifts the texture position along U. |
| **Offset Y** | Vertical UV offset — shifts the texture position along V. |
| **Offset Z** | Z-axis UV offset for world-projection or triplanar Z face. |
| **use UV Rotation** | Enables rotation of the UV coordinates around the texture center. |
| **use World-Z Rotation** | Applies rotation using world Z-axis alignment. Only when World Projection is enabled. |
| **Rotation** | UV rotation angle in degrees. |
| **World-Z Rotation** | World-space Z rotation angle. |

---

### ♦ use World Projection

Enables world-space UV projection. Exposes triplanar, local, top-down, side, and smooth projection options.

<img src="images/image12.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **use Local Projection** | Snaps world projection to local object space — textures respond correctly to mesh transforms. |
| **Triplanar Projection** | Enables triplanar blending across all three axes — eliminates UV stretching on any surface angle. |
| **TopDown - use Side Projection** | Switches between top-down (Z-only) and side (X+Y combined) projection when Triplanar is OFF. |
| **use SmoothProjection** | Blends the seam between projection faces for a smoother transition without sharp edges. |
| **Blend Sharpness** | Controls how sharply the triplanar faces blend at their boundaries. |

<img src="images/image46.png" style="max-width:100%; border-radius:6px; margin-top:16px;">

---

### ♦ use UV Methods

Enables advanced UV method controls — Atlas, ObjectScale, Offset Variation, Tiling Variation, Animation, Fake Displacement, Fake Shadow, and Silhouette.

<img src="images/image75.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

#### use Atlas

<img src="images/image7.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **Atlas U Position** | Horizontal position within the atlas grid — selects the column. |
| **Atlas V Position** | Vertical position within the atlas grid — selects the row. |
| **Atlas Position Random** | Randomly offsets the atlas position per instance. |
| **Atlas Size** | Size of each cell in the atlas grid. |

<img src="images/image48.png" style="max-width:100%; border-radius:6px; margin-top:16px;">

#### use ObjectScale

<img src="images/image49.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **Object - use Axis Scale** | Uses a single selected axis scale value instead of uniform scale. |
| **Single - use both UV Channels** | Routes the scale calculation through both UV channels simultaneously. |
| **Scale U - use V Direction** | Applies the scale value to V direction instead of U. |
| **Axis Scale - U** | Selects which world axis (R=X, G=Y, B=Z) drives the U tiling scale. |
| **Axis Scale - V** | Selects which world axis drives the V tiling scale. |
| **Radius Scale** | Additional scale multiplier applied on top of the axis scale. |

#### use Offset Variation

| Parameter | Description |
|-----------|-------------|
| **useTrimSheet** | Limits offset variation to a single UV axis — required for trimsheets. |
| **Along X - use Y TrimDirection** | Switches the constrained trim axis from X to Y direction. |
| **use Atlas Offset** | Offsets variation within atlas cell boundaries. |
| **Atlas Offset Size** | Size of the offset step within the atlas. |

<img src="images/image41.png" style="max-width:100%; border-radius:6px; margin-top:16px;">

#### use Tiling Variation

<img src="images/image45.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **use Voronoi Projection** | Projects Voronoi cells in world space for consistent variation. |
| **use Tiling Variation Rotation** | Enables rotation within each Voronoi cell. |
| **use Voronoi Offset Single Direction** | Constrains Voronoi offset to a single UV direction. |
| **Voronoi Offset X - use Y** | Switches the constrained Voronoi offset axis from X to Y. |
| **Voronoi Scale** | Scale of the Voronoi cell pattern. |
| **Voronoi Mask Sharpness** | Controls the sharpness of the blend at Voronoi cell boundaries. |
| **Voronoi Offset** | Magnitude of the random UV offset per Voronoi cell. |
| **Voronoi Rotation** | Maximum rotation angle per Voronoi cell. `360.0` allows full random rotation. |

---

### ♦ use Animation

Enables UV animation for dynamic surfaces. Exposes Panner, Wave, and Bulge animation modes.

#### use Panner

<img src="images/image56.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **use Frequency** | Adds frequency modulation to the panner — creates pulsed scroll. |
| **Frequency along X** | Applies frequency modulation only along the X axis. |
| **Speed** | Global scroll speed. |
| **Random Speed Amount** | Adds a random speed offset per instance. |
| **Speed X** | Scroll speed along U axis. |
| **Speed Y** | Scroll speed along V axis. |

#### use Wave

<img src="images/image74.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **Amplitude** | Height of the wave oscillation. |
| **Frequency** | Number of wave cycles. |
| **Random Frequency Amount** | Randomizes wave frequency per instance. |

#### use Bulge

| Parameter | Description |
|-----------|-------------|
| **Bulge Amount** | Strength of the bulge deformation. Positive = outward, negative = inward. |

---

### ♦ use Fake Displacement

Enables Parallax Occlusion Mapping — simulates depth by ray-marching the height map without actual geometry displacement.

<img src="images/image27.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description | Default |
|-----------|-------------|---------|
| **Parallax - use BumpOffset** | Switches from full POM to a simpler single-sample bump offset — cheaper. | — |
| **Height Ratio** | Depth scale for the POM effect. | — |
| **Height Contrast** | Sharpens or softens the height map used for POM. | — |
| **Max Steps** | Maximum ray-march iterations. Higher = better quality at steep angles. | — |
| **Steps Dither** | Adds dithering to the step count — reduces stair-stepping artifacts. | — |
| **Referance Plane** | Sets the reference depth plane. `0.5` is centered. | — |

---

### ♦ use Fake Shadow

Enables height-based fake shadow — simulates contact shadow using the height map without ray tracing.

<img src="images/image58.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **Shadow Height** | Depth range over which the fake shadow is cast. |
| **Shadow Sharpness** | Controls the hardness of the fake shadow edge. |
| **Shadow Steps** | Number of steps used to compute the fake shadow ray. |
| **Shadow Strength** | Intensity of the fake shadow — `0.0` = no shadow, `1.0` = full darkening. |
| **Sun - use custom LightVector** | Uses a custom light direction instead of deriving from scene lighting. |
| **Light Vector** | Custom light direction vector when `use custom LightVector` is ON. |

---

### ♦ use Parallax MeshClip

Clips the POM effect at mesh silhouette edges — prevents parallax from extending beyond the mesh boundary.

| Parameter | Description |
|-----------|-------------|
| **MeshClip Strength** | Controls how aggressively the parallax is clipped toward the mesh edge. |

---

### ♦ use Parallax Silhouette

Enables silhouette-aware POM — adjusts parallax at grazing angles to preserve edge believability.

<img src="images/image61.png" style="max-width:100%; border-radius:6px; margin-bottom:16px;">

| Parameter | Description |
|-----------|-------------|
| **Silhouette EdgeClip** | Controls the falloff range for silhouette-based parallax clipping. |
