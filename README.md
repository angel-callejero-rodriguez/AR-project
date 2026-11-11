# AR-project: first prototype of Reality Concept 3D

> 🇵🇹 O primeiro protótipo da Reality Concept 3D: uma página de loja de exemplo onde o produto abre em 3D e em realidade aumentada.

This is where [Reality Concept 3D](https://www.realityconcept3d.com) started (October 2026). It is a single-page mock furniture store that tests the core idea: a shopper on a product page taps **"Ver em 3D"**, rotates the piece in 3D and, on a phone, places it in their own room at real size with augmented reality (AR).

## What it shows

- **Product page with a 3D pop-up.** A plain HTML store page opens a modal with Google's `<model-viewer>`.
- **AR on any phone.** WebXR, Android Scene Viewer and iPhone Quick Look, with `ar-scale="fixed"` and floor placement, so the furniture can't be stretched.
- **Desktop to phone handoff.** On a computer, "Ver no smartphone" shows a QR code. Scanning it opens the page in AR mode (`?ar=true`), which hides the store and goes straight to the model.

No framework and no build step: plain HTML, CSS and a few lines of JavaScript.

## Run it

Serve the folder with any static server, for example:

```bash
npx serve .
```

AR needs HTTPS and a compatible phone, so test AR on a deployed copy (e.g. GitHub Pages), not on localhost.

## Files

| File | What it is |
|---|---|
| `index.html` | Store page, 3D modal, QR pop-up and AR-mode logic |
| `style.css` | Store page styles |
| `*.glb` | Demo furniture models |
| `foto-cadeira.png` | Product photo |

## Where it went next

The prototype grew into two production projects:

- [realityconcept3d](https://github.com/angel-callejero-rodriguez/realityconcept3d): the company website (Next.js), with private 3D/AR demo pages for each store.
- [rc3d-server](https://github.com/angel-callejero-rodriguez/rc3d-server): a 3D/AR server that any store website can use with one line of code, plus a model pipeline.

## Author

Built by **Angel Rodriguez**, founder of Reality Concept 3D.
