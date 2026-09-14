# sadbodhs.github.io

Landing page for the deep learning studies — served at **https://sadbodhs.github.io/**.

A single self-contained `index.html`. No build step, no dependencies: GitHub Pages
serves the file as-is (`.nojekyll` keeps Jekyll out of the way).

## Topics

| Topic | Status | Site |
|---|---|---|
| Computer Vision — Inference Serving | Live | [computer_vision_optimization](https://sadbodhs.github.io/computer_vision_optimization/) |
| Language & Multimodal Models | In preparation | — |
| Training & Fine-tuning | In preparation | — |
| Deployment & MLOps | In preparation | — |

Each topic is its own repository with its own site, deployed independently. This
repo only holds the hub that links them.

## Adding a topic

Topic cards live in the `#topics` grid in `index.html`. To promote a placeholder
to live, replace its `<div class="card placeholder">` block with the `<a class="card live">`
pattern used by the CV card: status pill, title, `sub` line for the hardware and model,
a description, a `finding` blockquote, three headline `stat` figures, tags, and the link.

Then update the `count` in the section header.

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy

Push to `main`, then enable Pages in repo settings: **Settings → Pages → Source:
Deploy from a branch → `main` / `(root)`**. No Actions workflow needed.
