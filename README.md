# Notion 3D Viewer

This is a simple 3D viewer that can be embedded in Notion as an iframe. It uses three.js to render the 3D model.

## How to use

Pass a url to a .glb file as shown below and it'll load the glb. I haven't extensively tested it but it'll load the glb in whatever embeds where iframe is supported. I needed this for Notion. Feel free to raise an issue for features and bugs.

## URL Parameters

To view a 3D model and configure its display, you can append query parameters to the viewer's URL. All parameters are optional.

**Base URL Example:**
`https://<your-username>.github.io/<your-repo-name>/`

**Parameters:**

*   `modelUrl`: **(Required)** The URL to your 3D model file (GLB or GLTF format). This must be a publicly accessible URL.
    *   **Example:** `?modelUrl=https://raw.githubusercontent.com/KhronosGroup/glTF-Sample-Models/refs/heads/main/2.0/Duck/glTF-Binary/Duck.glb`

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

[live demo](https://abhinay1997.github.io/Notion3DViewer/?modelUrl=https://raw.githubusercontent.com/KhronosGroup/glTF-Sample-Models/refs/heads/main/2.0/Duck/glTF-Binary/Duck.glb&theme=dark)

Sample duck.glb credits to KhronosGroup! Thanks team!

## Embedding in Notion

To embed the viewer in Notion, simply paste the constructed URL (including your `modelUrl` and any other desired parameters) into a Notion page and select "Embed".
