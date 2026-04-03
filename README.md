# Color Sampling in QGIS 🎨

Bridge the gap between vintage cartography and modern GIS by reverse-engineering professional color palettes from historical maps. This repository provides a custom QGIS processing model designed to capture the "DNA" of printed masterpieces and integrate their sophisticated color logic into the digital workspace.

---

## 📖 Detailed Guide
For a full step-by-step tutorial, including the historical context of the 1928 Iceland map used in this workflow, please visit the official blog post:
👉 **[Color Sampling in QGIS | Staridas Geography](https://www.staridasgeography.gr/blog/color-sampling-in-qgis/)**

---

## 🛠 Included Resources

* **Color_Sampling.model3**: The core processing model that automates pixel extraction across multiple dimensions, including RGB, HSV, CMYK, and HEX.
* **Color_Sampling.qml**: A specialized style file that provides "instant styling," allowing sampled points to automatically adopt the color of the underlying map pixel.

## 🚀 Professional Workflow

### 1. Preprocessing
* **Add Model**: Open the QGIS Processing Toolbox and use "Add Model to Toolbox" to load the `.model3` file.
* **Source Map**: Load your reference raster and rename the layer to **'Map'** (this naming is vital for postprocessing automation).
* **Sampling Layer**: Create a New Temporary Scratch Layer (Point geometry) to serve as the vehicle for your sampling locations.

### 2. Execution
* Run the **Color Sampling** model, inputting your 'Map' raster, your scratch points, and the `.qml` style file.
* The model generates a "Sampled Colors" layer with a comprehensive attribute table containing R, G, B, H, S, V, C, M, Y, K, and HEX values.

### 3. "Live" Sampling & Automation
* Set a layer variable named `source_map` to the value **'Map'** to enable a fluid "pick-and-move" workflow.
* QGIS will automatically recalculate all color data the moment a point is added or moved to a new location.

---

## 📄 License & Credits
* **Author**: [Staridas Geography](https://www.staridasgeography.gr/blog/color-sampling-in-qgis/) #MakingMapsPretty
* **Website**: [www.staridasgeography.gr](https://www.staridasgeography.gr)
* **License**: CC BY-NC-ND 4.0
* **Copyright**: 2026 | All Rights Reserved
