# Ratnesh GitHub Profile README

This folder is designed to become the special GitHub profile repository:

`https://github.com/ratneshbuilds03/ratneshbuilds03`

## Publish it

1. Create a **public** repository named exactly `ratneshbuilds03` under `ratneshbuilds03`.
2. Upload the **contents of this folder**, not the outer folder itself.
3. Commit `README.md` to the `main` branch.
4. Open `https://github.com/ratneshbuilds03`. GitHub automatically shows a profile README when the repository name matches the username.

## What's included

- `assets/hero-3d.svg` — animated isometric backend command-center hero with the supplied portrait rendered as a dot-matrix visual.
- `assets/architecture-3d.svg` — animated API/data/cache/cloud system map.
- `assets/stack-3d.svg` — animated technology-stack signal panel.
- `assets/radar-*.svg` — backend focus radars.
- `assets/card-stats-*.svg` — self-hosted GitHub snapshot cards.
- `assets/portrait.svg` — reusable animated dot-matrix portrait.

## Refresh workflow

The included GitHub Action regenerates the radar SVGs and GitHub snapshot cards when the related JSON files change, on pushes to `main`, and on its scheduled run.

## Local regeneration

If you change `assets/skills.json` or `assets/langmix.json`:

```bash
python scripts/radar.py --data assets/skills.json -o assets/radar
python scripts/radar.py --data assets/langmix.json -o assets/radar-langs --values
```

The premium hero is hand-authored SVG so its animation and layout stay deterministic. If you replace the portrait, update `assets/portrait.svg` and regenerate/embed it in `assets/hero-3d.svg` as needed.
