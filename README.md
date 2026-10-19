# Albika IRP — Personal Portfolio

A personal portfolio website documenting my coding knowledge and projects, plus a
suite of small interactive tools.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Main portfolio — landing page, profile, projects, and contact |
| `apps.html` | Interactive utilities suite (includes an AC capacity & electricity cost simulator) |

Both pages are **fully self-contained**: all CSS and JavaScript is inlined, so they
can be opened directly in a browser with no build step and no CDN dependencies.

## Viewing locally

No installation is required. Just open the file:

```bash
xdg-open index.html     # Linux
```

Or serve the directory over HTTP (recommended, so relative links resolve cleanly):

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Optional: Vite / React dev server

The repository also contains a Vite + React + TypeScript + Tailwind scaffold
(`src/`, `package.json`, `vite.config.ts`). **This is currently unused** — the live
pages are the standalone HTML files above and do not load `src/main.tsx`.
It is kept for future work if the site is migrated to a component-based build.

```bash
npm install
npm run dev      # http://localhost:3000
npm run build    # outputs to dist/
npm run lint     # type-check only (tsc --noEmit)
```

## Environment variables

An optional `.env.example` documents two variables used by AI Studio:

- `GEMINI_API_KEY` — required only for Gemini AI features
- `APP_URL` — the host URL, used for self-referential links

Real `.env*` files are git-ignored (`.env.example` is the only one tracked).

## Notes / known follow-ups

- The profile image still points at a placeholder (`picsum.photos`) and should be
  replaced with a real photo.
- Footer copyright still reads `© 2025`.

## License

Apache-2.0 (see the SPDX headers in `src/`).
