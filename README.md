# browser Studio 1018

**browser Studio 1018** is a browser-extension experience that turns a pile of open tabs into a focused product-thinking brief. It is designed as a portfolio-ready new-tab workspace: collect sources, surface a local insight, and leave with clear next moves.

## Features

- A polished extension-style brief workspace with realistic product-research content.
- Searchable tab collection (press `/`), accessible checkboxes, keyboard Escape handling, focus states, responsive layout, empty state, feedback toasts, and modal insight exploration.
- Local “Studio Signal” demo mode: the product communicates an AI-like synthesis without an API key or paid service.
- Included Manifest V3 configuration. Load `dist/` as an unpacked extension after building, or use the app as a standalone new-tab-inspired web demo.

## Setup

```bash
npm install
npm run dev
```

Run `npm run build` for a production build and `npm test` for the lightweight behavior-model test.

## Architecture

- `src/main.jsx` contains the interactive React UI and local demo data/state.
- `src/styles.css` contains the responsive design system and component styling.
- `public/manifest.json` is the Chromium Manifest V3 extension descriptor.

No backend is needed: all demo data and synthesis are local. `.env.example` reserves a place for an optional future integration and contains no secrets.

## Screenshots / representation

For portfolio screenshots, run the dev server at a desktop width (1440px is ideal) and capture the main “Creator tools, reframed” brief. Also capture the “Explore the signal” modal and a mobile viewport to show the responsive behavior. The interface is original work and uses fictional demo content.

## Deployment notes

The Vite production output is static and works on any static host. For Chromium extension testing, run `npm run build`, navigate to `chrome://extensions`, enable Developer mode, choose **Load unpacked**, and select `dist/`. Browser APIs are intentionally not required for the demo; a production capture flow can connect the listed `tabs` and `storage` permissions.
