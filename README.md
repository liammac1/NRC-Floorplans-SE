# Ottawa Marriott Hotel — Traced 3D Reconstruction

An interactive 3D model of the Ottawa Marriott Hotel, built by digitizing wall
geometry directly from the hotel's scanned public-area exit/fire-safety floor
plans (9 floors: Lower Level 2, Lower Level 1, Main Lobby, 2nd–4th floors, and
the 27th–29th tower floors).

**[View the live demo](#)** ← replace with your GitHub Pages URL once published,
e.g. `https://<username>.github.io/<repo>/`

## What it is

- Every wall shown is a real traced line segment extracted from the source
  PDF via computer-vision line detection (OpenCV), not a hand-drawn
  approximation.
- Elevator cores (amber) and exit stairs (red) are highlighted; faint columns
  in the stacked view show the stairs running as continuous vertical shafts.
- Floors 5–26 (guest rooms) aren't in the source drawing set, so they're shown
  as a translucent placeholder mass between the traced podium and tower floors.

## Running locally

This is a single self-contained `index.html` (Three.js is loaded from
cdnjs at runtime — no build step, no dependencies to install). Just open it
in a browser, or serve the folder with any static file server:

```bash
python3 -m http.server 8000
```

## Publishing to GitHub Pages

1. Push this folder's contents to a GitHub repo (root, or a `/docs` folder).
2. Repo Settings → Pages → set the source branch/folder.
3. Your model will be live at `https://<username>.github.io/<repo>/`.

## Source

Drawings: "Public Area Exit Floor Plans," Project No. 99097.3, Leber/Rubes
Inc. Not to scale — a schematic, dimensionally-approximate reconstruction of
the traced wall layout.
