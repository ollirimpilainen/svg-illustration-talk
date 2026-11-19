# Drawing with numbers

A designer talk about making SVG illustrations with Claude: instead of asking for one image, ask Claude for a program that draws every image in a series by the same rules.

The talk is one long scrolling page (`index.html`). Demos from five client projects (GRK, BCE, Finmatec, Luotokoti, Kaskipuu) are embedded as iframes from `demot/`, and scrolling the talk drives their animations through `postMessage`. The files the demos need (CSS, JS, fonts, images) are copied under `assets/`, mirroring each project's own folder structure, so all paths are relative.

Live version: https://ollirimpilainen.github.io/svg-illustration-talk/

## Run locally

The page must be served over HTTP (not opened as a file), so the iframes share one origin:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000/ and scroll.

The Kaskipuu demo loads three.js from cdn.jsdelivr.net, and the talk loads the Outfit font from Google Fonts, so an internet connection is needed for those.
