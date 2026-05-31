# 🔍 Detail

Ambient Occlusion, Normal map intensity, and Detail Normal layers for adding micro-surface complexity.

---

### ♦ use AO

Enables the Ambient Occlusion system for the layer.

| Parameter | Description |
|-----------|-------------|
| **Packed - use Combined AO** | Reads AO from a packed channel combining base and detail AO — reduces texture bandwidth. |
| **Packed - use Detail AO** | Sources AO from a dedicated detail AO packed channel. |
| **AO Min** | Minimum clamp for AO output. Negative values push AO darker than source allows. |
| **AO Max** | Maximum clamp for AO output. Controls the brightest occluded area. |
| **AO** | Selects the texture channel carrying the AO data. Red channel is standard for packed ORM. |

---

### Base Normal

| Parameter | Description |
|-----------|-------------|
| **Normal Intensity** | Multiplier for normal map strength. `1.0` is full intensity. |
| **use Normal from Height** | Derives the normal map from the height/displacement channel instead of a baked normal texture. |

---

### ♦ use Detail Normal

Enables a secondary detail normal map layered on top of the base normal.

| Parameter | Description |
|-----------|-------------|
| **use Detail Normal World Projection** | Projects the detail normal in world space — prevents stretching on steep surfaces. |
| **use Detail Normal Rotation** | Enables rotation control for the detail normal texture. |
| **Detail Normal Texture** | The normal map texture asset used for the detail pass. |
| **Detail Normal Intensity** | Blend strength of the detail normal over the base normal. |
| **Detail Normal Tiling** | UV scale multiplier for the detail normal. |
| **Detail Normal Rotation** | Rotation angle for the detail normal UV. |

---

### ♦ use Detail Normal - 2

Enables a second independent detail normal layer — allows two separate micro-surface passes at different scales or angles.

| Parameter | Description |
|-----------|-------------|
| **Detail Normal Texture-2** | Texture asset for the second detail normal pass. |
| **Detail Normal Intensity - 2** | Blend strength of the second detail normal. |
| **Detail Normal Tiling-2** | UV scale for the second detail normal — set differently from the first to break repetition. |
| **Detail Normal Rotation-2** | Rotation angle for the second detail normal UV. |
