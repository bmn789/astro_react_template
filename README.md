# Astro React Template

Astro site with **React** islands, **Tailwind CSS v4** (Vite plugin), and **shadcn/ui**-style components (`components.json`).

## Prerequisites

- [Node.js](https://nodejs.org/) 20+ (LTS recommended)

## Clone and install

```sh
git clone https://github.com/bmn789/astro-react-template project_name
cd project_name
npm install
```

## Start developing

```sh
npm run dev
```

The dev server listens on **http://localhost:3000** (see `astro.config.mjs`).

| Command           | Description                          |
| ----------------- | ------------------------------------ |
| `npm run dev`     | Local development                    |
| `npm run build`   | Production build to `./dist/`      |
| `npm run preview` | Serve the production build locally   |
| `npm run astro`   | Astro CLI (e.g. `npm run astro check`) |

## Stack in this repo

- **[Astro](https://docs.astro.build/)** — pages and layouts under `src/pages/` and `src/layouts/`.
- **[React](https://react.dev/)** — `@astrojs/react`; use `.tsx` components where you need client interactivity (`client:*` directives as needed).
- **[Tailwind CSS v4](https://tailwindcss.com/docs)** — configured via `@tailwindcss/vite` in `astro.config.mjs`; global styles in `src/styles/global.css`.
- **shadcn/ui** — `components.json` points UI to `src/components/ui` and utilities to `src/lib/utils.ts`. Path alias `@/` maps to `src/` (see `tsconfig.json` and Vite `resolve.alias`).

### Adding shadcn components

From the project root (where `components.json` lives):

```sh
npx shadcn@latest add button
```

Replace `button` with the [component](https://ui.shadcn.com/docs/components) you need. Import in Astro or React using the `@/` alias, for example `@/components/ui/button`.

## Learn more

- [Astro + React](https://docs.astro.build/en/guides/integrations-guide/react/)
- [Tailwind v4 with Vite](https://tailwindcss.com/docs/installation/using-vite)
- [shadcn/ui](https://ui.shadcn.com/docs)
