# Notion 3D Viewer

This is a simple 3D viewer that can be embedded in Notion as an iframe. It uses three.js to render the 3D model.

## How to use

1.  **Create a GitHub Repository:** Create a new public repository on GitHub.
2.  **Upload Files:** Add the `index.html` file to this repository.
3.  **Enable GitHub Pages:** In the repository's settings, go to the "Pages" section and enable GitHub Pages for the `main` branch.

Once GitHub Pages is enabled, the site will be available at `https://<your-username>.github.io/<your-repo-name>/`.

## URL Parameters

To view a 3D model and configure its display, you can append query parameters to the viewer's URL. All parameters are optional.

**Base URL Example:**
`https://<your-username>.github.io/<your-repo-name>/`

**Parameters:**

*   `modelUrl`: **(Required)** The URL to your 3D model file (GLB or GLTF format). This must be a publicly accessible URL.
    *   **Example:** `?modelUrl=https://raw.githubusercontent.com/mrdoob/three.js/dev/examples/models/gltf/DamagedHelmet/glTF-Binary/DamagedHelmet.glb`

*   `surface`: Toggles the visibility of the model's surface.
    *   **Allowed values:** `true`, `false`
    *   **Example:** `&surface=false` (to hide the surface)

*   `wireframe`: Toggles the visibility of the model's wireframe.
    *   **Allowed values:** `true`, `false`
    *   **Example:** `&wireframe=true` (to show the wireframe)

*   `color`: Sets the color of the wireframe. Use a hexadecimal color code (without the `0x` prefix).
    *   **Allowed values:** `000000` (black), `ff0000` (red), `00ff00` (green), `0000ff` (blue)
    *   **Example:** `&color=ff0000` (to set wireframe color to red)

*   `theme`: Sets the theme of the viewer (background and menu).
    *   **Allowed values:** `light`, `dark`
    *   **Example:** `&theme=dark` (to enable dark mode)

**Full URL Example:**

`https://<your-username>.github.io/<your-repo-name>/?modelUrl=https://raw.githubusercontent.com/mrdoob/three.js/dev/examples/models/gltf/DamagedHelmet/glTF-Binary/DamagedHelmet.glb&surface=true&wireframe=true&color=00ff00&theme=dark`

## Embedding in Notion

To embed the viewer in Notion, simply paste the constructed URL (including your `modelUrl` and any other desired parameters) into a Notion page and select "Embed".