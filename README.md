# fanoos-data

Static files read by the **Fanoos (فنّوس)** Android app
(`com.salmanabdallah.islam`, developer: Salman Abdallah), served by GitHub Pages.

- `api/v1/` — a read-only mirror of the app's API as JSON files, written by
  `infra/static/export.mjs` in the app's repository. A request path maps to a
  file name with `:` written as `-` and `.json` appended, e.g.
  `quran/ayahs/2:255/tafsir` → `api/v1/quran/ayahs/2-255/tafsir.json`.
- `app-version.json` — the latest published build, for the in-app update notice.
- `privacy.html` — the app's privacy policy.

## Sources and licences

- **Quran text** — Tanzil Project (tanzil.net), Creative Commons Attribution 3.0;
  verbatim copies only, with the source indicated. The full terms travel in
  `api/v1/quran/bundle/manifest.json` and are shown in the app.
- **Tafsir** — التفسير الميسر, King Fahd Glorious Quran Printing Complex;
  attribution travels with every entry.
- **Tajweed annotations** — cpfair/quran-tajweed, CC BY 4.0; terms in
  `api/v1/quran/tajweed/manifest.json`.

The text files here must not be edited by hand: the app verifies the Quran
bundle against the checksum in its manifest.
