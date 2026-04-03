# Color Sampling in QGIS 🎨

Bridge the gap between vintage cartography and modern GIS by reverse-engineering professional color palettes from historical maps. This repository provides a custom QGIS processing model designed to capture the "DNA" of printed masterpieces and integrate their sophisticated color logic into the digital workspace[cite: 2].

## 🛠 Included Resources

*   **Color_Sampling.model3**: The core processing model that automates pixel extraction across multiple dimensions, including RGB, HSV, CMYK, and HEX[cite: 2].
*   **Color_Sampling.qml**: A specialized style file that provides "instant styling," allowing sampled points to automatically adopt the color of the underlying map pixel[cite: 2].

---

## 🚀 Professional Workflow

This workflow uses high-resolution historical maps (such as the 1928 lithographic map of Iceland) as a reference to create functional digital palettes[cite: 2].

### 1. Preprocessing
*   **Add Model**: Open the QGIS Processing Toolbox and use "Add Model to Toolbox" to load the `.model3` file[cite: 2].
*   **Source Map**: Load your reference raster and rename the layer to **'Map'** (this specific naming is vital for postprocessing automation)[cite: 2].
*   **Sampling Layer**: Create a New Temporary Scratch Layer (Point geometry) to serve as the vehicle for your sampling locations[cite: 2].

### 2. Execution
*   Run the **Color Sampling** model from the Processing Toolbox, inputting your 'Map' raster, your scratch points, and the `.qml` style file[cite: 2].
*   The model generates a "Sampled Colors" layer featuring a comprehensive attribute table with R, G, B, H, S, V, C, M, Y, K, and HEX values[cite: 2].

### 3. "Live" Sampling & Automation
*   Set a layer variable named `source_map` to the value **'Map'** to enable a fluid "pick-and-move" workflow[cite: 2].
*   When the "Attributes Form" is configured with default values that trigger on update, QGIS will automatically recalculate all color data the moment a point is added or moved to a new location[cite: 2].

---

## 📊 Results
By sampling colors across varying elevations or features and sorting the data by the **Hue (H)** field, you can mathematically reconstruct historic gradients, preserving the aesthetic soul of original prints for modern mapping projects[cite: 2].

## 📄 License & Credits
*   **Author**: Staridas Geography #MakingMapsPretty[cite: 2]
*   **Website**: [www.staridasgeography.gr](https://www.staridasgeography.gr)[cite: 2]
*   **License**: CC BY-NC-ND 4.0[cite: 2]
*   **Copyright**: 2026 | All Rights Reserved[cite: 2]
