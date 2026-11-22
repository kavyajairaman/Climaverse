# ClimaVerse — Global Impact Atlas

This student-friendly website has three navigable views:

1. World map with clickable country outlines and country search.
2. Country dashboard with eight categories: Environment, Human health, Financial impact, Wildlife, Marine life, Quality of life, Water, Food & farming.
3. Deep-dive research pages for each category and country.

## Open

Open `index.html` in a browser. Both `index.html` and `country-data.js` must be in the same folder. No framework, API key, account, or build step required.

## Important data limitation

**This is a functional prototype, not yet a fully populated country impact database.** The map displays **17 verified ND-GAIN 2024 vulnerability scores** (on a 0–100 scale by multiplying the original 0–1 scores by 100). Other mapped countries are gray but clickable, and the country picker includes roughly 250 countries/territories. The Natural Earth 110m sample boundary dataset used for the map contains 176 non-Antarctica map features, so some small island nations and territories are not drawn on the map; these can still be selected in the search list.

ND-GAIN vulnerability is based on climate exposure, sensitivity, and adaptive capacity; **it does not directly measure observed damage or total impact.** The dashboard categories contain scientifically grounded explanations and suggested indicators; they are **not yet country-specific measured values**. Never show invented numbers for missing indicators.

## Complete the country scores

1. Download the University of Notre Dame ND-GAIN official country index data: https://gain.nd.edu/our-work/country-index/download-data/
2. Extract the official archive and find the 2024 `vulnerability.csv` (name/location may differ by release).
3. Extract ISO 3166-1 alpha-3 country codes and the 2024 vulnerability column. Check the scale (0–1 versus 0–100) and year.
4. Update the `window.VERIFIED_SCORES` object in `country-data.js`, retaining decimal fractions between 0 and 1. For example `"NOR":0.26348`.
5. Confirm the matching year and citation. Many small territories may have no ND-GAIN score, in which case keep them gray, never invent a value.

For a fully country-specific dashboard, research and store source-linked indicators separately for each category, noting units, country, year, and methodology.

Sources:
- ND-GAIN Country Index methodology: https://gain.nd.edu/our-work/country-index/methodology/
- ND-GAIN official data: https://gain.nd.edu/our-work/country-index/download-data/
- Publicly mirrored 2024 vulnerability table (initial verified entries): https://nationsinquiry.com/datasets/climate-vulnerability/2024
- IPCC Sixth Assessment (Impacts): https://www.ipcc.ch/report/ar6/wg2/
- Natural Earth public-domain country geometry (sample supplied with pyogrio testing fixtures): https://www.naturalearthdata.com/

## Publish free with GitHub Pages

1. With a parent/guardian/teacher if needed, create a GitHub account.
2. Create a repository named `climaverse`.
3. Upload `index.html`, `country-data.js`, and `README.md` together to the repository root.
4. Under Settings → Pages, deploy from `main` branch, root folder.
5. Your published address follows `https://USERNAME.github.io/climaverse/`.

No visitor account, tracking, cookies, forms collecting personal information, or database are included.
