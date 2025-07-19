# Notion 3D Viewer

This is a simple 3D viewer that can be embedded in Notion as an iframe. It uses three.js to render the 3D model.

## How to use

1.  **Create a GitHub Repository:** Create a new public repository on GitHub.
2.  **Upload Files:** Add the `index.html` file to this repository.
3.  **Enable GitHub Pages:** In the repository's settings, go to the "Pages" section and enable GitHub Pages for the `main` branch.

Once GitHub Pages is enabled, the site will be available at `https://<your-username>.github.io/<your-repo-name>/`.

To view a 3D model, you will need to append the `modelUrl` query parameter to the URL. For example:

`https://<your-username>.github.io/<your-repo-name>/?modelUrl=<URL-to-your-3d-model>`

The model must be a GLB or GLTF file and must be accessible via a public URL.

## Embedding in Notion

To embed the viewer in Notion, simply paste the URL with the `modelUrl` query parameter into a Notion page and select "Embed".
