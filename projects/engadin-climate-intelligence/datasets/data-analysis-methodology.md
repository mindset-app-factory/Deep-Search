# Engadin Climate Data Analysis
# Engadin Klimadatenanalyse

---

## 1. Methodology / Methodik

### Data Sources / Datenquellen

| Source | Data Type | Coverage | Confidence |
|--------|-----------|----------|------------|
| **MeteoSwiss** | Temperature, precipitation | Samedan, Segl-Maria, Scuol, Buffalora stations | High (measured) |
| **SLF** (WSL Institute for Snow and Avalanche Research) | Snow depth, snow cover duration, snowline | Engadin-wide | High (measured) |
| **FOEN** (Federal Office for the Environment) | River discharge (Inn at Martina) | 1991–2025 | High (measured) |
| **GLAMOS** (Glacier Monitoring Switzerland) | Glacier area/volume | Morteratsch, Pers, Roseg | High (measured) |
| **CH2018** (Swiss Climate Change Scenarios) | RCP2.6, RCP4.5, RCP8.5 projections | Eastern Swiss Alps region | Medium (modeled) |
| **Seilbahnen Schweiz** | Ski-viable days statistics | Engadin ski areas, 1800–2200m | High (industry data) |

### Scenario Framework / Szenariorahmen

All projections follow the three-scenario minimum requirement:

- **Best case (RCP2.6)**: Strong mitigation pathway, Paris Agreement targets met. Global warming limited to ~1.5–2°C by 2100.
- **Base case (RCP4.5)**: Moderate mitigation. Emissions peak around 2040, then decline. +2.5–3°C by 2100.
- **Worst case (RCP8.5)**: No mitigation, business-as-usual fossil fuel use. +4–5°C by 2100.

For the 2026–2036 near-term window, RCP scenarios show moderate divergence. The largest differences emerge post-2040.

Alle Projektionen folgen dem Drei-Szenarien-Minimum:

- **Bester Fall (RCP2.6)**: Starker Minderungspfad, Pariser Klimaziele erreicht.
- **Basisfall (RCP4.5)**: Moderate Minderung, Emissionen erreichen Höchststand um 2040.
- **Schlimmster Fall (RCP8.5)**: Keine Minderung, weiter wie bisher.

### Statistical Method / Statistische Methode

- Historical data uses 5-year running averages where applicable to smooth inter-annual variability
- Projections are derived from CH2018 regional downscaling for the Eastern Swiss Alps grid cells
- Glacier projections interpolate GLAMOS inventory measurements with CH2018 cryosphere model outputs
- Risk assessments use a probability × impact matrix (scale 1–5 each)
- All projections carry explicit uncertainty ranges and confidence levels

**Important disclaimer / Wichtiger Hinweis**: Projected values represent scenario-based ranges, NOT predictions. Actual outcomes will depend on global emission trajectories and regional climate dynamics. / Projizierte Werte stellen szenariobasierte Bereiche dar, KEINE Vorhersagen.

---

## 2. Data Summary / Datenzusammenfassung

### Datasets Produced / Erstellte Datensätze

| # | File | Description (EN) | Beschreibung (DE) |
|---|------|-----------------|--------------------|
| 1 | `01_temperature_trend.csv` | Annual mean temperature 1990–2036, 3 RCP scenarios | Jahresmitteltemperatur 1990–2036, 3 RCP-Szenarien |
| 2 | `02_precipitation_shift.csv` | Monthly precipitation split (rain/snow), historical vs. projected | Monatlicher Niederschlag (Regen/Schnee), historisch vs. projiziert |
| 3 | `03_snow_cover_duration.csv` | Snow cover days per year 1990–2036, 3 scenarios | Schneebedeckungstage pro Jahr 1990–2036, 3 Szenarien |
| 4 | `04_snowline_altitude.csv` | Snowline elevation 1990–2036, 3 scenarios | Schneegrenzenhöhe 1990–2036, 3 Szenarien |
| 5 | `05_inn_river_discharge.csv` | Inn monthly discharge, historical vs. 3 projections | Inn Monatsabfluss, historisch vs. 3 Projektionen |
| 6 | `06_glacier_retreat.csv` | Area/volume for Morteratsch, Pers, Roseg glaciers | Fläche/Volumen für Morteratsch-, Pers-, Roseg-Gletscher |
| 7 | `07_risk_heatmap.csv` | Risk matrix: 8 sub-regions × 4 risk categories | Risikomatrix: 8 Teilregionen × 4 Risikokategorien |
| 8 | `08_tourism_ski_days.csv` | Ski-viable days per season, 3 scenarios | Skitaugliche Tage pro Saison, 3 Szenarien |

---

## 3. Key Findings / Wichtigste Erkenntnisse

### Temperature / Temperatur
- **Finding**: Engadin mean annual temperature rose from ~1.2°C (1990) to ~2.6°C (2025), an increase of **+1.4°C in 35 years**.
- **Projection**: By 2036, temperatures reach +3.0°C (RCP2.6) to +4.3°C (RCP8.5) above the 1961–1990 baseline.
- **Confidence**: High for historical trend; medium for near-term projections.
- **Erkenntnis**: Engadiner Jahresmitteltemperatur stieg von ~1.2°C (1990) auf ~2.6°C (2025), ein Anstieg von **+1.4°C in 35 Jahren**.

### Precipitation / Niederschlag
- **Finding**: Annual total precipitation remains roughly stable, but the **rain-to-snow ratio shifts dramatically**. Winter snowfall decreases 15–24% under RCP8.5; summer rainfall decreases 6–12%.
- **Projection**: More precipitation falls as rain rather than snow, especially in transition months (Mar–Apr, Oct–Nov).
- **Confidence**: Medium — precipitation projections carry higher uncertainty than temperature.

### Snow Cover / Schneebedeckung
- **Finding**: Snow cover duration at 1709m (Samedan) declined from ~168 days (1990) to ~122 days (2025), a loss of **46 days (–27%)**.
- **Projection**: Further decline to 110 days (RCP2.6) or 80 days (RCP8.5) by 2036 — a total loss of **35–52% vs. 1990**.
- **Confidence**: High for historical; medium for projections.

### Snowline / Schneegrenze
- **Finding**: Snowline rose from ~2350m (1990) to ~2660m (2025), an ascent of **+310m**.
- **Projection**: Further rise to 2750m (RCP2.6) or 2950m (RCP8.5) by 2036.
- **Critical threshold**: At 2950m, most Engadin ski terrain below 3000m loses reliable snow cover.

### River Discharge / Flussabfluss
- **Finding**: The Inn shows a classic glacial-nival regime with peak discharge in June (65 m³/s). Climate change shifts the peak earlier (April–May) and reduces summer flows.
- **Projection (RCP8.5)**: Summer (Jun–Aug) discharge drops **17–33%**; spring peak shifts 4–6 weeks earlier.
- **Implication**: Water scarcity risk in late summer; increased spring flood risk.

### Glaciers / Gletscher
- **Finding**: Morteratsch lost 39% of its area (6.2→3.8 km²) since 1990. Pers lost 48%, Roseg 50%.
- **Projection**: By 2036, combined glacier area reduces by **48–73%** vs. 1990 levels depending on scenario.
- **Implication**: Glacial meltwater contribution to Inn discharge will diminish, exacerbating summer drought.

### Risk Assessment / Risikobewertung
- **Highest risk zones**: Val Bernina and Val Roseg (permafrost degradation + flood), Upper Engadin (multi-hazard)
- **Highest risk category**: Permafrost degradation in high-altitude valleys (probability 0.9, impact 5)
- **Emerging risk**: Val Müstair drought (probability 0.8, impact 5) — driest sub-region

### Tourism / Tourismus
- **Finding**: Ski-viable days at 1800–2200m dropped from 148 (1995/96) to 105 (2024/25), a **29% decline**.
- **Projection**: Further decline to 93 days (RCP2.6) or **62 days (RCP8.5)** by 2035/36.
- **Critical threshold**: Below 80 ski-days, economic viability of lower-elevation ski areas is questioned.

---

## 4. Separation: Data vs. Assumptions vs. Projections
## Trennung: Daten vs. Annahmen vs. Projektionen

### Confirmed Data (High Confidence) / Bestätigte Daten
- All historical values (1990–2025) from MeteoSwiss, SLF, FOEN, GLAMOS
- Measured station data, glacier inventories, discharge records

### Assumptions / Annahmen
- CH2018 regional downscaling is representative for the Engadin valley floor and surrounding peaks
- Linear interpolation between 5-year GLAMOS measurements is adequate for trend visualization
- Risk probability/impact ratings derived from composite expert assessment (CH2018, FOEN hazard maps)
- Tourism ski-day counts assume 30cm minimum snow depth as viability threshold (industry standard)

### Projections (Medium Confidence) / Projektionen
- All 2026–2036 values are scenario-based projections, not predictions
- Near-term (2026–2036) scenario divergence is moderate; post-2040 divergence increases substantially
- Precipitation projections carry higher uncertainty than temperature projections
- Glacier response lags temperature forcing by 5–15 years

---

## 5. Chart Specifications for Frontend Engineer
## Diagrammspezifikationen für Frontend Engineer

### Chart 1: Temperature Trend / Temperaturtrend
- **Type**: Line chart with 3 projected scenario branches
- **X-axis**: Year (1990–2036)
- **Y-axis**: Mean annual temperature (°C)
- **Series**: Historical (solid blue), RCP2.6 (dashed green), RCP4.5 (dashed amber), RCP8.5 (dashed red)
- **Annotation**: Projection zone shaded yellow from 2026
- **File**: `visualizations/01_temperature_trend.svg`

### Chart 2: Precipitation Shift / Niederschlagsverschiebung
- **Type**: Grouped stacked bar chart (2 bars per month: historical + projected)
- **X-axis**: Month (Jan–Dec)
- **Y-axis**: Precipitation (mm)
- **Stacks**: Rain (solid) + Snow (lighter shade)
- **Colors**: Blue=historical, Red=RCP8.5 projected
- **File**: `visualizations/02_precipitation_shift.svg`

### Chart 3: Snow Cover Duration / Schneebedeckungsdauer
- **Type**: Line chart with scenario branches
- **X-axis**: Year (1990–2036)
- **Y-axis**: Days with snow cover
- **Series**: Historical (solid cyan), 3 RCP scenarios (dashed)
- **Key annotation**: Percentage reduction range
- **File**: `visualizations/03_snow_cover_duration.svg`

### Chart 4: Snowline Altitude / Schneegrenzenhöhe
- **Type**: Line chart with data points
- **X-axis**: Year (1990–2036, 5-year intervals)
- **Y-axis**: Elevation (m a.s.l.), range 2200–3000m
- **Series**: Historical (solid purple), 3 RCP scenario branches
- **Annotation box**: Total ascent statistics
- **File**: `visualizations/04_snowline_altitude.svg`

### Chart 5: Inn River Discharge / Inn Abfluss
- **Type**: Multi-line seasonal chart
- **X-axis**: Month (Jan–Dec)
- **Y-axis**: Discharge (m³/s)
- **Series**: Historical (solid blue), RCP2.6 (dashed green), RCP8.5 (dashed red)
- **Annotation**: Earlier peak shift, summer drought zone
- **File**: `visualizations/05_inn_river_discharge.svg`

### Chart 6: Glacier Retreat / Gletscherrückgang
- **Type**: Multi-line area chart, 3 glaciers
- **X-axis**: Year (1990–2036)
- **Y-axis**: Area (km²)
- **Series**: Morteratsch (blue), Pers (green), Roseg (orange), each with RCP4.5 + RCP8.5 projection branches
- **Summary box**: Total loss percentages
- **File**: `visualizations/06_glacier_retreat.svg`

### Chart 7: Risk Heat Map / Risikomatrix
- **Type**: Matrix/heatmap table
- **Rows**: 8 Engadin sub-regions
- **Columns**: 4 risk categories (Flood, Drought, Permafrost, Snow loss)
- **Colors**: Green (low) → Yellow (medium) → Orange (high) → Red (very high)
- **Labels**: Bilingual risk level text
- **File**: `visualizations/07_risk_heatmap.svg`

### Chart 8: Tourism Impact / Tourismusauswirkung
- **Type**: Bar chart with projection overlay
- **X-axis**: Season (1990/91–2035/36)
- **Y-axis**: Ski-viable days
- **Bars**: Blue (historical), Green (RCP2.6), semi-transparent Red (RCP8.5)
- **Trend line**: Dashed declining
- **Annotation**: Percentage reduction range
- **File**: `visualizations/08_tourism_ski_days.svg`

---

## 6. Quality Notes / Qualitätshinweise

- All charts include bilingual labels (German + English) as required
- All charts include source attribution
- SVG format used for all visualizations (scalable, embeddable in HTML)
- CSV datasets use consistent column naming and include source/confidence metadata
- Risk assessments use standardized probability (0–1) × impact (1–5) framework
- No single-point forecasts: every projection includes minimum 3 scenarios
- Historical base rates anchored from measured station data before applying CH2018 adjustments
