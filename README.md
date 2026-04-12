# ease-docs

MkDocs **Material** handbook for EASE **workflows** (Report Generation, Patents, Clinical Success, Signal Quality). The **home page** (`index.md`) is a **single page**: a short default view per workflow, then **Expand** notes that load the full hyperlinked narrative via snippets (`docs/includes/`). Workflow “Overview” nav entries link back to the same anchors on Home. Built for **GitHub Pages**.

## Local preview

```bash
cd ease-docs
python -m venv .venv
# If PowerShell blocks activation, use: .venv\Scripts\activate.bat (cmd) or:
# .\.venv\Scripts\python.exe -m pip install -r requirements.txt
pip install -r requirements.txt
mkdocs serve
```

Open `http://127.0.0.1:8000`.

## Build

```bash
mkdocs build
```

Output: `site/`.

## GitHub Pages

1. Create a repo (for example `ease-docs`) and push this tree to **`main`**.
2. **Settings → Pages → Build and deployment**: set **Source** to **GitHub Actions** (recommended), or allow **`gh-pages`** branch if you deploy manually.
3. The included workflow (`.github/workflows/deploy.yml`) runs `mkdocs build` and deploys the **`site/`** folder to the **`gh-pages`** branch (`peaceiris/actions-gh-pages`).
4. Edit **`mkdocs.yml`** → `site_url` to match `https://<user>.github.io/<repo>/`.

## Google Doc links

Replace placeholders in **`docs/workflows/patents/references.md`** (refs **1–6**) with your real document ID and heading links.

## License

Add a `LICENSE` file in the repo root if this handbook should be reusable by collaborators.
