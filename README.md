# Notion 3D Viewer

This is a simple 3D viewer that can be embedded in Notion as an iframe. It uses `three.js` to render 3D models.

## Features

- **Load Models via URL**: Pass a public URL to a `.glb` or `.gltf` file.
- **Upload Local Models**: Use the UI to load `.glb`, `.gltf`, or `.zip` files from your computer.
- **ZIP File Support (Experimental)**: Upload a `.zip` file containing your model (`.gltf`/`.glb`) and its textures. The viewer will automatically handle the file hierarchy.
- **Interactive Controls**: Orbit and inspect the model.
- **Customizable Display**: Toggle the model's surface and wireframe visibility.
- **Customizable Wireframe**: Change the color of the wireframe.
- **Light/Dark Mode**: Switch between themes for the viewer and its controls.
- **Auto-Rotate**: Automatically rotate the model for a dynamic view.
- **Embeddable**: Designed to be easily embedded in Notion or any site that supports iframes.

## How to use

You can either use the UI to upload a local file or pass a URL to a `.glb`/`.gltf` file in the query parameters. I needed this for Notion, but it will work in any embed that supports iframes. Feel free to raise an issue for features and bugs.

## URL Parameters

To view a 3D model and configure its display, you can append query parameters to the viewer's URL. All parameters are optional.

**Base URL Example:**
`https://<your-username>.github.io/<your-repo-name>/`

**Parameters:**

*   `modelUrl`: The URL to your 3D model file (`.glb` or `.gltf`). This must be a publicly accessible URL.
    *   **Example:** `?modelUrl=https://raw.githubusercontent.com/KhronosGroup/glTF-Sample-Models/refs/heads/main/2.0/Duck/glTF-Binary/Duck.glb`

*   `surface`: Toggles the visibility of the model's surface.
    *   **Allowed values:** `true`, `false`
    *   **Default:** `true`
    *   **Example:** `&surface=false` (to hide the surface)

*   `wireframe`: Toggles the visibility of the model's wireframe.
    *   **Allowed values:** `true`, `false`
    *   **Default:** `false`
    *   **Example:** `&wireframe=true` (to show the wireframe)

*   `color`: Sets the color of the wireframe. Use a hexadecimal color code (without the `0x` prefix).
    *   **Allowed values:** `000000` (black), `ff0000` (red), `00ff00` (green), `0000ff` (blue)
    *   **Default:** `000000`
    *   **Example:** `&color=ff0000` (to set wireframe color to red)

*   `theme`: Sets the theme of the viewer (background and menu).
    *   **Allowed values:** `light`, `dark`
    *   **Default:** `dark`
    *   **Example:** `&theme=light` (to enable light mode)

*   `autorotate`: Toggles automatic rotation of the model.
    *   **Allowed values:** `true`, `false`
    *   **Default:** `false`
    *   **Example:** `&autorotate=true` (to enable auto-rotation)

**Full URL Example:**

[live demo](https://abhinay1997.github.io/Notion3DViewer/?modelUrl=https://raw.GithubUserContent.com/DRx3D/glTF-Sample-Models/main/Models/GlassHurricaneCandleHolder/glTF-Binary/GlassHurricaneCandleHolder.glb&theme=dark&lighting=true&environment=true&autorotate=true)

![full screen](https://github.com/Abhinay1997/Notion3DViewer/blob/main/assets/full.png?raw=true)
Sample duck.glb credits to KhronosGroup! Thanks team!

## Embedding in Notion

To embed the viewer in Notion, simply paste the constructed URL (including your `modelUrl` and any other desired parameters) into a Notion page and select "Embed". Here's how it looks on Notion:
![notion](https://github.com/Abhinay1997/Notion3DViewer/blob/main/assets/notion_iframe.png?raw=true)
