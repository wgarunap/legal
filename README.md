# Legal

Terms of use, privacy policies and the Impressum for my apps, served by GitHub Pages at https://wgarunap.github.io/legal/.

## Add an app

1. Add an entry to `_data/apps.yml` (slug, name, tagline, summary, platforms, accent colours, support email).
2. Create a folder named after the slug with `icon.png` (180 px), `index.md`, `terms.md`, `privacy.md` and `impressum.md`. Copy the front matter from `setjot/`.

The Impressum text is shared: `_includes/impressum.md`.

SetJot's pages are generated from the app (`tool/export_legal_site.py` in the setjot repo) in English at `setjot/<page>` and seven more languages at `setjot/<code>/<page>`. The app opens them with `?embed=1&theme=light|dark`, which hides site navigation and uses the app's colours.
