# Label Lab Webpage

Premium B2B manufacturing website for Label Lab, built with Astro.

The site positions Label Lab as a high-end industrial solutions partner covering CAB automatic labeling systems, seamless welding PU logos, precision die-cut parts, printed labels, packaging materials, and roll label supply.

## Tech Stack

- Astro
- TypeScript strict mode
- Component-based UI architecture
- Static output for GitHub Pages

## Project Structure

```text
src/
  layouts/
    BaseLayout.astro
  components/
    Header.astro
    Footer.astro
    Hero.astro
    ProductBento.astro
    ProductCard.astro
    DetailPage.astro
  pages/
    index.astro
    details/
      barcode-label.astro
      package-materials.astro
      poron-diecut.astro
      print-label.astro
      seamless-welding.astro
      thermal-label.astro
  styles/
    global.css

public/
  images/
  favicon.svg
```

## Development

Install dependencies:

```bash
npm install
```

Run the local dev server:

```bash
npm run dev
```

Local URL:

```text
http://127.0.0.1:4321/labellab_webpage/
```

## Build

```bash
npm run build
```

Preview the production build:

```bash
npm run preview
```

## Quality Check

```bash
npm exec astro check
```

## GitHub Pages

The Astro config is prepared for GitHub Pages:

```js
export default defineConfig({
  site: "https://theacestore.github.io",
  base: "/labellab_webpage",
  output: "static",
});
```

Deployment is handled by:

```text
.github/workflows/deploy.yml
```

Pushing to `main` triggers the GitHub Pages deployment workflow.

## Notes

- Current production source lives in `src/` and `public/`.
- Root-level legacy HTML files are no longer the primary source for the Astro site.
- Static image assets used by Astro are stored in `public/images/`.
