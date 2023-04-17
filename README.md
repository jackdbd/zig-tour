# Zig tour

Talk I gave at [pisa.dev](https://pisa.dev/).

https://zig-tour.vercel.app/

## Installation

```sh
npm install
```

## Development

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

Slidev allows [exporting the slides to a PDF](https://sli.dev/guide/exporting.html#pdf). This feature relies on [Playwright](https://playwright.dev/) and requires [playwright-chromium](https://www.npmjs.com/package/playwright-chromium) to work. Since I did not want to install Playwright when building on Vercel (so deployments are faster), I declared it as a dev dependency and set `npm install --omit=dev` as the Vercel `installCommand` in `vercel.json`.

Run this command to export the slides to `assets/zig-tour.pdf`:

```sh
npm run export:pdf
```
