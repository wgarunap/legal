# Legal

Terms of use, privacy policies and the Impressum for my apps, served by GitHub Pages at https://wgarunap.github.io/legal/.

## Add an app

1. Add an entry to `_data/apps.yml` (slug, name, tagline, summary, platforms, accent colours, support email).
2. Create a folder named after the slug with `icon.png` (180 px), `index.md`, `terms.md`, `privacy.md` and `impressum.md`. Copy the front matter from `setjot/`.

The Impressum text is shared: `_includes/impressum.md`.

SetJot's pages are generated from the app (`tool/export_legal_site.py` in the setjot repo) in English at `setjot/<page>` and seven more languages at `setjot/<code>/<page>`. The app opens them with `?embed=1&theme=light|dark`, which hides site navigation and uses the app's colours.

## SetJot updates

The app reads `setjot/version.json` when it opens. Edit it only after a release is live in **both** stores.

- `latest`: the newest version. Older apps show the what's-new sheet once per version.
- `minimum`: older apps must update before they can be used. Raise it only for a serious bug.
- `app_store`, `play_store`: the store pages (`https://apps.apple.com/app/id<APP ID>`, `https://play.google.com/store/apps/details?id=com.euappsolutions.setjot`). While one is empty, that platform shows nothing.
- `slides`: one per new feature, swiped sideways. `image` is a 16:10 picture under `setjot/whats-new/`; `title` and `body` hold one text per language code (`en`, `de`, …). A language that is missing falls back to English. With no slides, the sheet says "SetJot <latest> is here".

```json
{"latest": "1.1.0", "minimum": "1.0.0",
 "app_store": "https://apps.apple.com/app/id<APP ID>",
 "play_store": "https://play.google.com/store/apps/details?id=com.euappsolutions.setjot",
 "slides": [{"image": "whats-new/rest-timer.png",
             "title": {"en": "Rest timer on lock screen"},
             "body": {"en": "See your rest countdown without unlocking your phone."}}]}
```
