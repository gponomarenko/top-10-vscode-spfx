# Top 10 VS Code Extensions for SPFx Development

A simple static website listing the top 10 Visual Studio Code extensions every SharePoint Framework (SPFx) developer should have.

## Repository structure

```
.
├── index.html      # Main page – replace with your prepared HTML
├── css/
│   └── style.css   # Base stylesheet
├── assets/         # Images and other static assets
└── .gitignore
```

## Publishing with GitHub Pages

The repository includes a GitHub Actions workflow (`.github/workflows/deploy.yml`) that automatically builds and deploys the site to GitHub Pages on every push to `main`.
Before deployment, the workflow now runs a smoke test that serves the static site and verifies the homepage title string so broken publishes are blocked.

### One-time setup

1. Go to **Settings → Pages** in this repository.
2. Under **Source**, select **GitHub Actions**.
3. Push to `main` (or trigger the workflow manually) — your site will be live at  
   `https://<username>.github.io/top-10-vscode-spfx/`.
4. Open the Actions run and confirm both jobs succeed:
   - `validate` (smoke test)
   - `deploy` (GitHub Pages publish)

> The workflow also has a **workflow_dispatch** trigger so you can deploy manually from the **Actions** tab at any time.

## Local preview

Open `index.html` directly in a browser, or use any static file server, e.g.:

```bash
npx serve .
```
