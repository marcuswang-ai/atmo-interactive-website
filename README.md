# Rising Tides: How the Coastline Changes, 1900–2100

An interactive map that shows which coastal land, cities and towns end up below the water line as global sea level changes from 1900 to 2100. Type in a country (or leave it blank for the world), then use the sliders to change:

- **Year** (1900–2100): measured sea level before 2020, projections after.
- **Warming by 2100** (−5 °C to +5 °C vs. pre-industrial): sets how fast sea level rises after 2020, using a fit to the IPCC AR6 scenarios.
- **Storm surge** (optional, 0–5 m): temporary extra water from a storm and high tide on top of the average sea level.

The map colours dry land that falls below the water level, marks cities by whether their centre is below, near or above the water, and updates two charts and a city table live.

**Live site:** https://marcuswang-ai.github.io/atmo-interactive-website/

**Group members:** Marcus Wang, Samuel Sebastian DeGroot, Randy Yanes

## How it works

- Sea level 1900–2020: Frederikse et al. (2020, *Nature*) and NASA satellite altimetry.
- Sea level 2020–2100: rise by 2100 = 0.198 m + 0.130 m × warming (°C), fitted to IPCC AR6 WG1 SPM projections (within 1–2 cm of all five scenario medians).
- Elevation: Terrain Tiles (Mapzen / AWS Open Data). Countries and cities: Natural Earth. Base map: OpenStreetMap / CARTO.
- It is a simple "bathtub" model: it ignores sea walls, local land sinking, regional differences in sea-level rise, and errors in the elevation data. See the "Limitations" section on the page.

## Running it

It is one file, `index.html`, with no build step. Open it in a browser, or publish it with GitHub Pages (Settings → Pages → Deploy from branch → `main` / root). It needs an internet connection to load the map tiles, elevation data and city list.

