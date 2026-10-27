# THEK Digital site

Public marketing / portfolio site for **THEK Digital Limited** (`thekdigital.com`).

This repository is **site-only**. It holds Astro pages, CSS, and public-safe diagrams or video. Private FPGA HDL, Vivado projects, bitstreams, XSA, and `.elf` files stay in private repositories and are never published here.

## Local development

Requires Node.js 22+.

```bash
npm install
npm run dev
```

Build:

```bash
npm run build
npm run preview
```

## Content structure

Single long homepage with sticky nav:

1. **Hero** — FPGA LLM on ALINX AX7A200B (Artix-7), ~25–28 tok/s proof point
2. **Featured** — iDelay/TDC and PCIe XDMA DAQ cards
3. **Projects** — one-line blurbs
4. **About** / **Contact**

Diagram and Manim slots under `public/placeholders/` are clearly marked for real assets later.

## GitHub Pages

A ready-to-use Actions workflow is checked in as `docs/github-pages-deploy.yml` (not under `.github/workflows/` yet, because the push token lacked the `workflow` scope).

To enable Pages:

1. Copy `docs/github-pages-deploy.yml` to `.github/workflows/deploy.yml` (needs a token or account with the `workflow` scope, or paste it in the GitHub UI).
2. Repo **Settings → Pages → Build and deployment → Source: GitHub Actions**
3. Push to `main` (or run the workflow manually)

Preview URL once enabled: `https://tttdddtmdavid.github.io/thekdigital-site/`

Custom domain (`thekdigital.com`) and GoDaddy DNS changes are a later step; do not point DNS until the Pages preview looks right.

## Brand rules

- Brand: **THEK Digital** (not Tech Vision)
- MediaHub: out
- No lab-LAN URLs
- No links into private GitHub trees
- UK English
