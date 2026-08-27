# Frame Mockup & Cost Estimator

A single-file web app for picture framers. Upload a photo of your artwork and a
straight-on photo of a moulding sample strip; get a live frame mockup with
mitered corners, an optional mat, and a material cost / customer price estimate.

No backend, no dependencies, no build step — everything is in `index.html`.

## Deploy to GitHub Pages

**Option A — dedicated repo:** commit `index.html` to the repo root, then enable
Pages (Settings → Pages → Deploy from branch → `main` / root).

**Option B — subfolder of an existing repo:** put `index.html` in `/docs`, then
point Pages at the `/docs` folder.

Either way the app works at whatever Pages URL results — no paths are hardcoded.

## Usage notes

- Photograph the moulding sample **horizontally, straight-on**; the top edge of
  the photo is treated as the *outer* edge of the frame. Use the "Flip moulding"
  checkbox if your photo is the other way up.
- Pricing profiles (cost/ft, markup, waste %, labor add-on, mat defaults) are
  saved in the browser's `localStorage`. Images are never stored.
- Cost math: outer frame = artwork + 2×mat + 2×face; total moulding is the
  outer perimeter (the miter long points *are* the outer dimensions), plus a
  user-adjustable waste percentage (15% default).

## Sample images

`samples/` contains a generated test artwork and moulding strip for trying the
app without real photos. They are not required for deployment.
