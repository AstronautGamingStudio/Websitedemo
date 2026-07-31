# Aether Chronos Website

A cinematic, high-end static landing page for **Aether Chronos**, a luxury mechanical and smart-hybrid watch brand. The experience is dependency-free at runtime and uses HTML, CSS, and Canvas animation so it is easy to run, host, and deploy on almost any static platform.

## What is included

- Full-screen hero with the headline **“Time, Perfected”** and a glassmorphism CTA panel.
- Animated canvas watch centerpiece with studio-style lighting, dust particles, ticking hands, scroll-responsive orbiting, and an exploded movement sequence.
- Craftsmanship feature cards for the Swiss movement, sapphire crystal, hybrid smart features, and premium hand-finished materials.
- Movement journey section with sticky editorial captions.
- Collection showcase with four Aether Chronos models and hover micro-interactions.
- Strap selector concept for Leather, Steel, and Rubber options.
- Minimal final CTA/footer section.
- Responsive layout for desktop, tablet, and mobile.

## Requirements

- Node.js 18+ for validation/build scripts.
- Python 3 for the built-in local static server.
- No npm package installation is required because the site has no external JavaScript dependencies.

## Quick start

```bash
npm run dev
```

Then open:

```text
http://127.0.0.1:5173/
```

If port `5173` is already in use, you can run a one-off server on another port:

```bash
python3 -m http.server 8000
```

Then open `http://127.0.0.1:8000/`.

## Validate and build

Run the JavaScript syntax check:

```bash
npm run check
```

Create a deployable static build:

```bash
npm run build
```

The deployable site is generated in:

```text
dist/
```

Preview the generated build locally:

```bash
npm run preview
```

Then open:

```text
http://127.0.0.1:4173/
```

## Deployment

Because this is a static website, deploy the project root or the generated `dist/` directory to any static host.

### Netlify

1. Connect the repository in Netlify.
2. Use this build command:

   ```bash
   npm run build
   ```

3. Use this publish directory:

   ```text
   dist
   ```

A `netlify.toml` file is included with these defaults.

### Vercel

1. Import the repository in Vercel.
2. Use this build command:

   ```bash
   npm run build
   ```

3. Use this output directory:

   ```text
   dist
   ```

A `vercel.json` file is included with these defaults.

### GitHub Pages

1. Run `npm run build` locally or in CI.
2. Publish the contents of `dist/` to GitHub Pages.
3. Keep `.nojekyll` in the published output if your workflow copies dotfiles.

## Project structure

```text
.
├── index.html          # Page structure and content sections
├── package.json        # Local development, validation, build, and preview scripts
├── scripts/build.mjs   # Dependency-free static build script
├── src/main.js         # Canvas animation and UI interactions
├── src/styles.css      # Responsive cinematic visual design
├── netlify.toml        # Netlify deployment defaults
└── vercel.json         # Vercel deployment defaults
```

## Customization tips

- Update section copy in `index.html`.
- Tune watch animation, scroll behavior, feature data, and collection data in `src/main.js`.
- Adjust colors, typography, spacing, and breakpoints in `src/styles.css`.
- For production brand typography, self-host licensed font files and replace the Google Fonts import in `src/styles.css`.
