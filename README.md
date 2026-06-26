# Agreaux — Project Site

The website and documentation for **Agreaux**, an open-source framework for building
**low-cost VR/AR digital twins** of industrial facilities using game-industry tools —
Blender, Godot and low-cost LiDAR. Developed by the **LSU Digital Twinning Lab**.

> Framework source code: https://github.com/lsudigitaltwinninglab/agreaux

This repo hosts the **static site** (served via GitHub Pages): a project overview, the
pipeline/architecture diagrams, and a documentation overview of the workflow and tools.

## What is Agreaux?

Agreaux turns a real plant into an interactive 3D digital twin you can explore in virtual
and augmented reality. Capture a site with a low-cost LiDAR scanner (e.g. Eagle) and photogrammetry, register
it into a scaled point cloud, model it 1:1 in Blender, and deploy a multiplayer twin in Godot
on a Meta Quest 3 — at a fraction of traditional engineering cost. The reference build
digitizes the LSU distillation columns as an accessible, reproducible demo.

### Highlights

- **VR, AR & toy-model modes** on Meta Quest 3 (OpenXR).
- **Multiplayer with QR-code spatial anchors** — co-located users share one aligned model.
- **P&ID with pointer interactions** linked to 3D equipment and metadata.
- **Guided modeling from scans** via the Point Cloud Visualizer & Plant Modeling Tools Blender add-ons + Geometry Nodes.
- **Interactive training tools** — ladder movement, walkable ramps, 3D drawing, category toggles.

### Open toolchain

Blender · Godot 4.6 · CloudCompare / RealityScan · OpenXR · Meta Quest 3 · Low-cost LiDAR (e.g. Eagle)

## Site structure

```
.
├── index.html          # Landing / overview page
├── docs.html           # Documentation: overview + architecture diagrams (Mermaid)
├── assets/
│   ├── css/style.css   # Styles
│   ├── js/main.js      # Nav, copy buttons, scroll-spy
│   └── img/favicon.svg # Favicon
├── .nojekyll           # Serve files as-is on GitHub Pages
├── github-repo/        # (local reference copy of the framework — not part of the site)
└── proposal-docs/      # (internal reference docs — not part of the site)
```

> **Note:** `github-repo/` and `proposal-docs/` are local reference material. If you don't
> want them published with the site, add them to `.gitignore` before pushing.

## Local preview

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

The architecture diagrams on the docs page render with [Mermaid](https://mermaid.js.org/)
loaded from a CDN, so a network connection is needed to see them.

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository.
2. In **Settings → Pages**, set the source to the `main` branch (root).
3. The site publishes at `https://<user>.github.io/<repo>/`.

## License

Agreaux is an open-source project. The specific license structure is still being decided and
will be announced once finalized.
