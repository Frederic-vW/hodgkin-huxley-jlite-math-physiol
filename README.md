# The Hodgkin–Huxley model of the action potential

An interactive notebook for neuroscience students, built on the Hodgkin–Huxley model from Chapter 5
(Excitability) of Keener & Sneyd, *Mathematical Physiology*, 3rd ed. (Springer, 2025).

**Run in your browser (no installation, JupyterLite):**
[open the notebook](https://<github-user>.github.io/<repo>/notebooks/index.html?path=hh.ipynb)

Open the notebook, then choose **Run ▸ Run All Cells**. The first run can take up to a minute while Python
loads in the browser. Your edits are stored in this browser only, so use **File ▸ Download** to keep a copy.

## Contents

- `hh.ipynb`: the Hodgkin–Huxley explorer, with Explore / Challenges / Key Ideas tabs. It is the only file
  published to the JupyterLite site.

## Build locally

```
pip install -r requirements.txt
jupyter lite build --contents hh.ipynb --output-dir dist
jupyter lite serve --output-dir dist
```

## Deployment

The GitHub Action in `.github/workflows/deploy.yml` builds the site and deploys it to GitHub Pages on every
push to the `jupyterlite` branch. In the repository settings, set **Pages ▸ Build and deployment ▸ Source**
to **GitHub Actions**.

## Sources

The model equations and parameter values are adapted from the authors' official code release,
https://github.com/jsneyd/Math-Physiol-3rd-Edition-code (`chap05_excitability/hh.py`, Fig. 5.6).
