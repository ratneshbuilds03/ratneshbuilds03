# Ratnesh GitHub Profile README

This folder is designed to become the special GitHub profile repository:

`https://github.com/ratneshbuilds03/ratneshbuilds03`

## Publish it

1. On GitHub, create a **public** repository named exactly `ratneshbuilds03` under the account `ratneshbuilds03`.
2. Upload the contents of this folder (not the outer folder itself).
3. Commit `README.md` to the `main` branch.
4. Open `https://github.com/ratneshbuilds03` and the profile README should appear automatically.

## Optional refresh workflow

The included GitHub Action regenerates the radar SVGs on pushes and on a daily schedule. The banner is already generated and committed, so no Python setup is required just to display the README.

## Local regeneration

If you change `assets/skills.json` or `assets/langmix.json`:

```bash
python scripts/radar.py --data assets/skills.json -o assets/radar
python scripts/radar.py --data assets/langmix.json -o assets/radar-langs --values
```

If you replace `assets/source/ratnesh.jpg`:

```bash
python scripts/banner/generate.py
```

The banner is an animated SVG. GitHub renders the SVG animation directly in the profile README.
