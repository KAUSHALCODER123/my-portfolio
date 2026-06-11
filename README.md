# portfolio-dashboard

Personal portfolio styled as a backend system dashboard. Astro + Tailwind v4, zero framework JS — all interactions are a single vanilla script.

```sh
npm run dev      # http://localhost:4321
npm run build    # static output in dist/
npm run preview  # serve the production build
```

## Where things live

| What | File |
|---|---|
| All routes/sections, drawer data, terminal log lines | `src/pages/index.astro` |
| Design tokens (colors, fonts) + every component style | `src/styles/global.css` |
| Head, fonts, meta | `src/layouts/Layout.astro` |

## Customizing

- **Project details** — edit the `projects` array (table rows) and the `PROJECTS` object (drawer content) in `index.astro`. Replace the `href: "#"` placeholders with real GitHub/demo links.
- **Skills** — edit the `skills` array at the top of `index.astro`.
- **Easter-egg log lines** — `TERM_LINES` in the same file.
- **Contact form** — currently simulates a `200 OK` (see the `TODO` in the submit handler). To make it real, drop in [EmailJS](https://www.emailjs.com/) or point `fetch` at a serverless endpoint, then keep the same response/toast UI.

## Deploying

Static output — works anywhere:

- **Vercel / Netlify**: import the repo, framework preset "Astro", done.
- **GitHub Pages**: `npm run build`, publish `dist/` (set `site`/`base` in `astro.config.mjs` if served from a subpath).
