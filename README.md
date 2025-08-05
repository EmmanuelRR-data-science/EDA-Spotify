# 🎧 Spotify 2023 — Análisis Exploratorio de Datos (EDA)

## 🎯 Objetivo
Analizar las características musicales y de popularidad de las canciones en Spotify en 2023, e identificar patrones mediante visualización y clustering.

---

## ✅ 1. Relaciones clave con la popularidad (`streams`)

- Las variables más fuertemente correlacionadas con `streams` fueron:
  - `in_spotify_playlists`: **+0.78**
  - `in_apple_playlists`: **+0.74**
  - `in_deezer_playlists`: **+0.61**

> 📌 *La inclusión en playlists, especialmente en Spotify, es el principal impulsor del número de reproducciones.*

---

## 📉 2. Características musicales vs Streams

| Variable musical     | Correlación con `streams` |
|----------------------|---------------------------|
| `danceability_%`     | -0.093                    |
| `energy_%`           | -0.036                    |
| `valence_%`          | -0.051                    |
| `speechiness_%`      | -0.099                    |

> ❗ *Las características musicales tienen una relación débil o incluso negativa con la popularidad. Canciones tranquilas o acústicas también pueden ser exitosas.*

---

## 🔗 3. Relaciones internas entre variables musicales

| Variables                            | Correlación |
|-------------------------------------|-------------|
| `valence_%` ↔ `energy_%`            | +0.35       |
| `danceability_%` ↔ `valence_%`      | +0.39       |
| `energy_%` ↔ `acousticness_%`       | -0.55       |

> 🎵 *Canciones felices suelen ser más energéticas; canciones acústicas suelen ser menos enérgicas.*

---

## 🤖 4. Clustering

### 🔹 Clustering 1: `streams` vs `in_spotify_playlists`
- Se identificaron **6 clústeres** con diferencias claras en exposición y popularidad.
- Las canciones con mayor número de reproducciones están altamente presentes en playlists.
- El clustering permite segmentar canciones por visibilidad digital.

### 🔹 Clustering 2: `valence_%` vs `energy_%`
- Se formaron **6 clústeres emocionales**:
  - Alta valence + alta energy → canciones alegres y animadas.
  - Baja valence + baja energy → canciones melancólicas o acústicas.
- Útil para recomendaciones musicales basadas en el estado de ánimo.

---

## 📌 Conclusión general

> La popularidad de una canción **no depende directamente de sus características musicales**, sino principalmente de su **exposición en playlists**.  
> Las características musicales, sin embargo, **permiten clasificar canciones por perfil emocional y sonoro**, lo que resulta útil para sistemas de recomendación.

---
