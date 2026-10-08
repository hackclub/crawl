# Crawl

The landing page for **Crawl**, a Hack Club You Ship, We Ship program: spend two or more hours building your own web crawler and get $10 toward a video game on Steam or Itch.io.

Built with Vue 3 and Vite. The page is a single static component (`src/App.vue`), with no routing or state.

## Development

```sh
npm install
npm run dev
```

## Build

```sh
npm run build
```

Output goes to `dist/`, which any static host can serve. Preview the production build locally with `npm run preview`.

## Where things live

- `src/App.vue`: all page content and styles. Sizes are in `rem`, so the whole page scales with the root `font-size` set on `html`.
- `src/assets/`: the web and spider artwork.
- `index.html`: meta tags, favicons and the Google Fonts link (Lora and Shadows Into Light).
- `public/`: favicons.

## TODO

- The "submit your project" button in `App.vue` is a placeholder (`href=""`).
