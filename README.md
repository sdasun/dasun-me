# dasun.me

Personal website built with Vue 3, TypeScript, Vite, and Tailwind CSS.

## Scripts

- `npm run dev`: Start local development server.
- `npm run build`: Build production assets to `dist/`.
- `npm run build:docs`: Build and sync output to `docs/` for GitHub Pages.
- `npm run preview`: Preview the production build locally.

## GitHub Pages deployment

This project is served from the `docs/` directory.

Use:

```bash
npm run build:docs
```

The sync command updates `docs/` and removes stale files, while preserving `docs/CNAME`.
