# PMK Internal Medicine pages

Each page lives in its own folder and is served by GitHub Pages at `https://icyice1998.github.io/pmk/<folder>/`. The root `index.html` links to them.

| Page | Folder | URL |
|---|---|---|
| Admission Report | `ar/` | https://icyice1998.github.io/pmk/ar/ |

## Admission Report (`ar/`)

Single-page dashboard for Internal Medicine Admission Report (AR) at Phramongkutklao Hospital.

- Reads the AR submission Google Sheet live (Form Responses 1 + Archive tabs) on every visit; HN is never loaded.
- Tabs: AR cases, Top Resident, Top Case (grouped by the Table of Specification 2568-2569), Top Consult, Current AR / By date, Top Ward.
- Year and month filters apply to every tab except Current AR / By date.

To add a page: create a new folder with its own `index.html`, then add a card for it in the root `index.html`.
