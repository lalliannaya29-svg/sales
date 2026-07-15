# Ledger — Excel & Power BI Document Vault

A single-page document library for storing and browsing Excel and Power BI
files, built with HTML5, [Bootstrap 5](https://getbootstrap.com/), and
[React 18](https://react.dev/) (loaded via CDN — no build step, no install).

## Features

- Drag-and-drop or click-to-upload for `.xlsx .xls .xlsm .csv .pbix .pbit`
- Automatic classification into Excel workbooks vs. Power BI reports
- Search, filter, and sort (recent / name / size)
- Folder-tab style document cards with real download support
- Fully responsive, no external framework build required

## Running it locally

No installation needed — it's a single static HTML file.

1. Clone the repo
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```
2. Open `index.html` directly in a browser, **or** serve it locally:
   ```bash
   python3 -m http.server 8000
   ```
   then visit `http://localhost:8000`.

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
4. Choose the `main` branch and `/ (root)` folder, then **Save**.
5. GitHub will publish the site at `https://<your-username>.github.io/<your-repo>/`.

## Notes on storage

This is a client-side demo: uploaded files live in the browser's memory for
the current session only and reset on page reload. For documents to persist
across visits or be shared between users, pair this frontend with a backend
(an API + database, or object storage such as S3 / Azure Blob).

## Project structure

```
.
├── index.html   # the entire app — markup, styles, and React code
└── README.md
```
