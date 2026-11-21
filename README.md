# PMK Internal Medicine pages

Each page lives in its own folder and is served by GitHub Pages at `https://icyice1998.github.io/pmk/<folder>/`. The root `index.html` links to them.

| Page | Folder | URL |
|---|---|---|
| Admission Report | `ar/` | https://icyice1998.github.io/pmk/ar/ |
| CRO LSTM Report | `cro_lstm/` | https://icyice1998.github.io/pmk/cro_lstm/ |

## Admission Report (`ar/`)

Single-page dashboard for Internal Medicine Admission Report (AR) at Phramongkutklao Hospital.

- Reads the AR submission Google Sheet live (Form Responses 1 + Archive tabs) on every visit; HN is never loaded.
- Tabs: AR cases, Top Resident, Top Case (grouped by the Table of Specification 2568-2569), Top Consult, Current AR / By date, Top Ward.
- Year and month filters apply to every tab except Current AR / By date.

To add a page: create a new folder with its own `index.html`, then add a card for it in the root `index.html`.

## CRO LSTM Report (`cro_lstm/`)

Static technical report on LSTM models that predict carbapenem-resistant culture results (CRPA, CRAB, CRE, CRO).

- Plain HTML, CSS and JavaScript with no build step and no external requests (d3 v7 is in `assets/`).
- All figures and tables are drawn from `data/report-data.js`: aggregate model outputs, no patient identifiers. The datasets `shap_points` and `shap_temporal` hold SHAP values of individual explained patient-days as anonymous numbers.
- Filters (cohort, antibiotic class, direction, search, threshold) and the per-antibiotic temporal views run in the browser.
- Mobile layout: contents menu, sideways-scrolling tables with a fixed first column, charts that reflow on narrow screens, and dark mode.
