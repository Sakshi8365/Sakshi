# Sakshi Tiwari — Portfolio

[![Deploy to GitHub Pages](https://github.com/Sakshi8365/Sakshi/actions/workflows/pages.yml/badge.svg)](https://github.com/Sakshi8365/Sakshi/actions/workflows/pages.yml)

Live site: https://sakshi8365.github.io/Sakshi/

A fast, responsive, and accessible portfolio built with plain **HTML, CSS, and JavaScript**.
Projects are rendered from a simple JSON file, so adding new work is quick and doesn’t require a build step.

![Portfolio preview](<assets/Screenshot 2026-03-11 100017.png>)

## Highlights

- **Responsive + accessible**: keyboard-friendly navigation, skip link, and readable contrast.
- **Data-driven projects**: cards are generated from `data/projects.json`.
- **Light/Dark theme**: preference stored in `localStorage` with a one-click toggle.
- **Performance-friendly effects**: automatically reduces heavy visual effects on low-power devices / reduced-motion settings.
- **Zero-build**: no framework, no bundler — deploy as static files.

## Tech stack

- HTML5
- CSS (CSS variables + modern responsive layout)
- Vanilla JavaScript (fetch + progressive enhancement)
- GitHub Pages (via GitHub Actions)

## Project structure

```text
.
├─ index.html              # Page structure + SEO meta
├─ css/
│  └─ styles.css           # Theme + layout
├─ js/
│  └─ script.js            # Theme + projects rendering + effects
├─ data/
│  └─ projects.json        # Projects content
└─ assets/                 # Images + resume
```

## Customize

### Update projects

Edit `data/projects.json`.

Supported fields:

- `title` (string)
- `description` (string)
- `tech` (array of strings)
- `source` (optional URL)

### Update profile content

Edit `index.html`:

- Hero text, “About”, Experience, socials
- SEO / social preview meta (`og:url`, `og:image`, etc.)
- Resume link (`assets/resume.pdf`)

### Update styling

Edit `css/styles.css`:

- Colors + theme variables
- Spacing + typography
- Component styling (cards, buttons, layout)

## Run locally

Because the Projects section loads JSON using `fetch`, use a local server (opening via `file://` will block requests in many browsers).

### Option A: Python

```pwsh
python -m http.server 5173
```

Open http://localhost:5173

### Option B: Node

```pwsh
npx serve -p 5173
```

### Option C: VS Code Live Server

- Install the **Live Server** extension
- Right-click `index.html` → **Open with Live Server**

## Deploy

This repo includes a GitHub Actions workflow that deploys to GitHub Pages on every push to `main`.

In GitHub:

1. Repository → **Settings** → **Pages**
2. Set **Source** to **GitHub Actions**

## License

MIT
