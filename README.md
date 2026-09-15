# sadbodhs.github.io

Landing page for the deep learning bench — served at **https://sadbodhs.github.io/**.

It frames the work as a workshop rather than a portfolio: finished studies, the open
question queue, and the deployment topics that rarely get benchmarked.

A single self-contained `index.html`. No build step, no dependencies: GitHub Pages
serves the file as-is (`.nojekyll` keeps Jekyll out of the way).

## Layout

A lab-datasheet layout, deliberately not a centred card grid: a fixed left rail
(index + rig spec table + controls) beside full-width ruled content. Serif prose
against monospace structure, hairline rules, no border-radius, no shadows, and a
faint graph-paper ground drawn with two CSS gradients.

The rail collapses to a sticky top bar below 1000px. Topic figures collapse from a
right-hand column to a row below 1200px — above that the rail would squeeze the
prose column too narrow.

## Topics

| Topic | Status | Site |
|---|---|---|
| Computer Vision — Inference Serving | Live | [computer_vision_optimization](https://sadbodhs.github.io/computer_vision_optimization/) |
| Vision-Language Models | In preparation | — |
| VLA for Robotics | In preparation | — |
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

## The other sections

- **`#bench`** — the open question queue. Each `<li>` is a status chip (`design` /
  `queued` / `blocked`), a question, and why it matters. Nothing here may claim a
  number; move an item into a topic study once it has one.
- **`#gaps`** — "Things nobody benchmarks". A numbered grid of under-covered topics,
  mostly deployment and measurement-integrity ones.
- **House rules** — the bar a number has to clear before it gets published.

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy

Push to `main`, then enable Pages in repo settings: **Settings → Pages → Source:
Deploy from a branch → `main` / `(root)`**. No Actions workflow needed.
