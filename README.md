# U.S. Extreme Wet-Bulb Temperatures, 2005–2025

An interactive map of the highest wet-bulb temperatures recorded each year in 56 U.S. cities,
built from hourly NOAA NCEI Local Climatological Data (`FM-15` observations). Hover a city for its
peak, warming trend, and projection toward the empirical human-tolerance threshold; click for
year-by-year detail (single hottest hour and the mean of the three hottest days, with fitted trends).

The thresholds follow the 2022 Penn State study (Vecellio et al., *Journal of Applied Physiology*),
which found the real critical wet-bulb limit for healthy young adults is ~31 °C (≈87 °F) in humid
conditions — below the long-assumed 35 °C — and lower still, ~28 °C (≈82 °F), in dry heat. The map
applies both: 87 °F for humid cities, 82 °F for arid and semi-arid ones.

The page also discusses what a threshold day would mean in practice — outdoor trades, municipal
services, recreation, logistics, emergency response and cooling — and why the risk of an individual
threshold *hour* runs well ahead of the date any trend line crosses the line.

## Hosting

This is a single self-contained `index.html` (city data and U.S. map geometry are inlined; D3 loads
from a CDN). Any static host works — just serve `index.html` at the site root. `.nojekyll` is included
so GitHub Pages serves the file as-is.

## Data notes

- Source: NOAA NCEI LCD, 2005–2025, one primary airport station per city.
- "Highest recorded" = max hourly wet-bulb in the 2005–2025 window (not all-time).
- Trends are OLS slopes of annual maxima vs. year (low R² — illustrative, not forecasts).
- Projections extend that slope to the city's threshold, reported out to a 2100 horizon.
- Station substitutions: New York = LaGuardia · Dallas = Dallas–Fort Worth Intl · San Bernardino = Ontario Intl. Denver is missing 2013 (absent from the NCEI archive).
