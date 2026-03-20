# ranauro.giuliano — Personal Portfolio

Static site deployable on GitHub Pages. Zero build tools, zero dependencies (besides CDN-loaded libraries).

## Structure

```
ranauro.giuliano/
├── index.html                  ← Homepage (hero + project grid + about)
├── projects/
│   ├── project-template/
│   │   └── index.html          ← Copy this into every new project folder
│   ├── rag-chatbot-pipeline/
│   │   ├── index.html          ← Copied from template
│   │   └── README.md           ← Content rendered on the page
│   └── vending-locator/
│       ├── index.html
│       └── README.md
└── resources/                  ← Favicons (keep from old site)
```

## Adding a new project

1. Create a folder: `projects/my-project-name/`
2. Copy `projects/project-template/index.html` into it
3. Write a `README.md` in the same folder (supports full GFM: images, tables, code blocks)
4. Register the project in `index.html` inside the `PROJECTS` array:

```js
{
  slug: "my-project-name",   // must match the folder name
  name: "My Project",
  tag: "Category",
  desc: "Short description shown on the card.",
  accent: "#34d399"          // card accent color
}
```

That's it — no build step needed.

## Images in README

Place images inside the project folder and reference them with relative paths:

```md
![screenshot](screenshot.png)
```

## Test locally
Launch a simple HTTP server in the root folder:

```bash
python -m http.server 8000
```
