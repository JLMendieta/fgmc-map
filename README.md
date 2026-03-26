# Global FGM/C Prevalence Map

An interactive choropleth map visualising the prevalence of Female Genital Mutilation/Cutting (FGM/C) across countries worldwide. Built as a single self-contained HTML file — no server, no build step, no dependencies to install.

**Live map:** [https://JLMendieta.github.io/fgmc-map](https://JLMendieta.github.io/fgmc-map)

---

## About the Map

The map covers **42 countries** for which quantitative prevalence data is available. It is designed for use in presentations and educational settings. Countries are displayed on a neutral grey basemap and can be revealed one by one during an audience activity, or all at once.

Prevalence figures represent the **estimated national prevalence (%)** among women and girls. Where only sub-national or community-level data exists, figures have been normalised using demographic weighting (see Methodology below).

---

## Features

| Interaction | How |
|---|---|
| Click a country | Opens a detail panel with prevalence, legal status, source, and methodology |
| Reveal country colour | Clicking a country colours it on the prevalence scale |
| Navigate countries | `←` `→` arrow keys cycle through all countries alphabetically |
| Reveal all at once | **Reveal All** button in the top bar |
| Reset to grey | **Reset** button in the top bar |
| View sources | Press `S` |
| Close any panel | `Esc` or click outside |

### Colour scale

| Colour | Prevalence |
|---|---|
| Light orange | 0–10% |
| Orange-red | 10–25% |
| Red | 25–50% |
| Dark red | 50–80% |
| Deep red | 80%+ |

Countries with sub-national data only are shown with a **dashed border** once revealed.

---

## Data Sources

- **UNICEF 2024** — *Female Genital Mutilation: A Global Concern – 2024 Update.* New York: UNICEF. Primary source for 31 countries via nationally representative DHS/MICS surveys.
- **Time is Now 2025** — End FGM European Network, Equality Now & US End FGM/C Network. *The Time is Now: End FGM/C: An Urgent Need for Global Response.* Brussels/London/Washington DC.
- **Farouki et al. 2022** — "The Global Prevalence of FGM/C: A Systematic Review and Meta-analysis." *PLOS Medicine* 19(8): e1004061.
- **Primary field studies** — Ahmady (2015), Chibber et al. (2011), Rouzi et al. (2019), Thabet & Al-Kharousi (2018), Awar & Al-Jefout et al. (2020), Antonova & Siradzhudinova (2016), ONIC (2012), Anantnarayan, Diler & Menon (2018), Zambia Sexual Behaviour Survey (2009).

For full citations and methodology notes, press `S` inside the map.

---

## Methodology Note

Sub-national prevalence figures (communities or regions rather than whole countries) are normalised using:

```
Estimated National Prevalence = Community Prevalence × (Community Size / National Population)
```

This assumes 0% prevalence outside the studied community — a conservative lower bound. For Kuwait, Oman, Saudi Arabia, and the UAE, clinical or regional samples are used as a proxy for the national average. Full details are available in the country detail panels.

Diaspora/destination countries (USA, UK, Canada) are excluded — available data for these countries uses absolute numbers rather than population percentages and is not directly comparable.

---

## Technical Notes

- **Single file** — all data and logic are embedded in `index.html`; no external files required beyond the map tiles and GeoJSON borders (fetched from public CDNs at load time)
- **Map library** — [Leaflet.js](https://leafletjs.com/) 1.9.4
- **Basemap** — CartoDB Positron (no labels), via CARTO CDN
- **Country borders** — [datasets/geo-countries](https://github.com/datasets/geo-countries) GeoJSON via jsDelivr/GitHub

---

## Licence & Attribution

&copy; 2026 J.L. Mendieta — All rights reserved.

The underlying prevalence data belongs to the respective source organisations (UNICEF, Equality Now, End FGM European Network, and the authors of individual studies). This map is a visualisation tool compiled for educational and advocacy purposes.
