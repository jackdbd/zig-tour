# Zig tour

An introduction to the Zig programming language and toolchain.

I gave this talk at [pisa.dev](https://pisa.dev/).

- 🌐 https://zig-tour.vercel.app/
- 📺 https://www.youtube.com/live/Fe1xDUh6dYs
- 🗎 https://raw.githubusercontent.com/jackdbd/zig-tour/main/assets/zig-tour.pdf

## Installation

The presentation is  Vue.js application built with [Slidev](https://sli.dev/). You can install the dependencies with:

```sh
npm install
```

## Development

Slidev can hot-code reload your presentation thanks to Vite. Launch the dev server with:

```sh
npm run dev
```

Slidev Play mode:

http://localhost:3030/1

Slidev [Presenter](https://sli.dev/guide/presenter-mode.html) Mode:

http://localhost:3030/presenter/1

## Deploy

The `dist` directory will be automatically deployed to Vercel on each `git push`.

## PDF export

Slidev allows [exporting the slides to a PDF](https://sli.dev/guide/exporting.html#pdf). This feature relies on [Playwright](https://playwright.dev/) and requires [playwright-chromium](https://www.npmjs.com/package/playwright-chromium) to work. Since I did not want to install Playwright when building on Vercel (so deployments are faster), I declared `playwright-chromium` as a dev dependency and set `npm install --omit=dev` as the Vercel `installCommand` in `vercel.json`.

Run this command to export the presentation to `assets/zig-tour.pdf`:

```sh
npm run export:pdf
```

Note: exporting the notes with this command generates an empty PDF. Maybe a Slidev bug?

```sh
npx slidev export-notes --output assets/zig-tour-notes
```
