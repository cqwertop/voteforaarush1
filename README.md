# Anumukonda '26 — Campaign Site

A bold, animated one-page campaign site built with Astro for Aarush Anumukonda.

## Running it locally

You'll need [Node.js](https://nodejs.org) (v18+) installed.

```sh
npm install
npm run dev
```

Then open http://localhost:4321 in your browser. The page hot-reloads as you edit.

To build a static version you can host anywhere (or zip up for a teacher):

```sh
npm run build
```

That produces a `dist/` folder — open `dist/index.html` directly, or upload the whole
`dist/` folder to any static host (Netlify, Vercel, GitHub Pages, etc).

## What to customize

Everything lives in **`src/pages/index.astro`** — one file, top to bottom:

- **Candidate name / slogan** — edit the `<h1 class="hero-title">` lines near the top of the `<body>`
- **Platform planks** — edit the `platform` array at the very top of the file (four `{n, title, body}` objects)
- **Stats** — edit the `stats` array (the animated counters)
- **Timeline** — edit the `timeline` array
- **Candidate photo** — replace `public/images/candidate.jpg` with your own image (keep the same filename, or update the `src` in the `<img>` tag)
- **Colors** — all defined once at the top of the `<style>` block under `:root`: `--ink`, `--coral`, `--gold`, `--violet`, `--paper`

## What's interactive

- Nav bar shrinks and blurs on scroll
- Hero headline has a subtle parallax scroll effect
- Platform items, stats, and timeline entries fade/slide in as you scroll to them
- Stat numbers count up from 0 when they enter view
- Buttons have a "magnetic" cursor-follow effect on hover
- A scrolling marquee band in the hero

All motion respects `prefers-reduced-motion` for accessibility.

## Project structure

```
/
├── public/
│   └── images/
│       └── candidate.jpg   ← replace this with your photo
├── src/
│   └── pages/
│       └── index.astro     ← the whole site is here
└── package.json
```
