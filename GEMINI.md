## Project Understanding: Notion 3D Viewer

This project is a simple, embeddable 3D model viewer designed for use within Notion documents via an iframe. It leverages `three.js` to render GLB/GLTF models.

**Key Features:**
-   **Dynamic Model Loading:** Loads 3D models via a `modelUrl` query parameter or by uploading a local file. Supports `.glb`, `.gltf`, and `.zip` files (experimental) containing the model and textures.
-   **Interactive Controls:** Users can orbit the model.
-   **Toggleable Visuals:** Options to show/hide the model's surface and a wireframe overlay.
-   **Customizable Wireframe Color:** Users can select the wireframe color from predefined options.
-   **Theme Switching:** Supports light and dark mode for the viewer and its controls.
-   **URL-driven Configuration:** All menu options (surface, wireframe, color, theme, auto-rotate) can be pre-configured via URL query parameters for seamless embedding and sharing.
-   **Auto-Rotate:** Automatically rotate the model for a dynamic view.

**Technical Stack:**
-   HTML, CSS, JavaScript
-   `three.js` (from CDN)
-   `GLTFLoader.js` (from CDN)
-   `OrbitControls.js` (from CDN)

**Deployment:** Intended for GitHub Pages deployment.