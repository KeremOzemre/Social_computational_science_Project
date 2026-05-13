# Website — The US Politician Network

This folder contains the GitHub Pages site for the project.

## Files

- `index.html` — main single-page site (scrolling sections)
- `styles.css` — site styling (dark academic theme)
- `data/` — small downloadable datasets (copy `politicians_network_nodes2.csv` and `network.pkl` here)

## Enabling GitHub Pages

1. Push this `docs/` folder to your repository (any branch, but typically `main`).
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: `main` (or whichever branch holds `docs/`) → folder: `/docs`
4. Click **Save**. After ~1 min the site is live at `https://<username>.github.io/<repo-name>/`.

## Before going live — replace these placeholders

Search `index.html` for the following and replace them:

- `REPLACE_WITH_ONEDRIVE_LINK_FULL_TEXT` — public OneDrive/Drive link to `politicians_full_text.csv` (44 MB — exceeds the practical GitHub-Pages size, host externally)
- `REPLACE_WITH_ONEDRIVE_LINK_TOKENIZED` — public OneDrive/Drive link to `tokenized_wikipage.csv` (124 MB — exceeds GitHub's 100 MB hard limit, must be hosted externally)
- `REPLACE_WITH_NBVIEWER_LINK` — nbviewer URL to the explainer notebook
- `REPLACE_WITH_REPO` — your GitHub repo path, e.g. `lucas/Social_computational_science_Project`

## Adding the small data files

The project's `.gitignore` ignores `*.csv`, so copy the small files into `docs/data/` and force-add them:

```bash
mkdir -p docs/data
cp politicians_network_nodes2.csv docs/data/
cp network.pkl docs/data/
git add -f docs/data/politicians_network_nodes2.csv docs/data/network.pkl
```

(The 44 MB and 124 MB files should NOT go in the repo — host them on OneDrive/Drive and use the external links.)

## Filling in the "Coming soon" sections

The website is structured for the full project. Sections 03 (Network), 04 (Text), 05 (Communities), and 06 (Findings) have `Coming soon` placeholder blocks where the analyses will go. As each analysis is finished, replace its placeholder with figures and prose. Static images can live in `docs/assets/`; interactive plots can be embedded via inline SVG or `<iframe>`.
