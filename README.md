# Guided Liveness Capture

A small collection of static web demos for guided face liveness capture and a simple head viewer.

## Demo pages

- [liveness_ui.html](liveness_ui.html): Primary guided liveness UI — step-based checks (front, left, right, up, down). Uses the camera feed, simple brightness-based detection, a progress ring, and UI feedback.
- [liveness_3d.html](liveness_3d.html): 3D visualization variant that includes Three.js rendering and richer visual feedback.
- [head_viewer.html](head_viewer.html): Minimal Three.js head viewer (canvas + controls placeholder).

## Quick start

1. Serve the files from the project root (recommended). From PowerShell / terminal run:

```bash
python -m http.server 8000
```

or with Node.js:

```bash
npx http-server -p 8000
```

2. Open the demo in your browser:

http://localhost:8000/liveness_ui.html

Note: For camera access prefer `http://localhost`. Opening files via `file:///` may block `getUserMedia` in some browsers.

## How it works

- `liveness_ui.html` implements a step-by-step guided capture using a hidden canvas to read video frames and simple region-brightness heuristics to detect head turns and tilts.
- `liveness_3d.html` adds Three.js-based rendering for 3D visualization and success feedback.
- `head_viewer.html` exposes a canvas + minimal controls for rendering head geometry using Three.js.

## Development

- Files are static HTML with inline JavaScript. Tailwind CSS and Three.js are loaded from CDN.
- Edit the HTML files directly and reload the page to test changes.
- Useful tools: browser DevTools, Live Server (VS Code), or the simple Python/Node servers above.

## Notes

- Camera permissions require a secure context or `localhost` — some browsers disallow camera access from `file:///` URLs.
- Tested on modern Chromium-based browsers; behavior may vary by device and camera.

## Origins & Attribution

- Development order: `liveness_ui.html` was created first, then `head_viewer.html`, and finally `liveness_3d.html` which combines the two.
- Head model source: downloaded from Free3D — https://free3d.com/3d-model/femalehead-v4--971578.html
- Verify the model's license before redistributing or bundling it with this project. If you'd like, I can add a `LICENSE` file or include a local copy of the model (only if you have redistribution rights).

## License

No license included. Add a `LICENSE` file to specify usage terms (for example, MIT).

## Contact

Open issues or submit pull requests to improve demos or documentation.

