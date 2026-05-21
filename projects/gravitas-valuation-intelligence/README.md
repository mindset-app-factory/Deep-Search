# Gravitas Valuation Intelligence Platform

**Project:** Gravitas — Alpine AI Infrastructure AG Valuation Intelligence  
**Client:** Mindset Deep-Research-KI-Agentur  
**Date:** 2026-05-21  
**Status:** QA Approved — Ready for CEO Final Review

---

## Overview

This project delivers a comprehensive institutional-grade valuation intelligence platform for **Gravitas (Alpine AI Infrastructure AG)**, an AI datacenter developer in Graubünden, Switzerland. The platform covers comparable M&A analysis, multi-scenario DCF and market-multiple valuation, sovereign premium attribution, infrastructure scoring, and exit strategy modeling.

**Probability-weighted Enterprise Value: CHF 363M**  
(Bull: CHF 1,062M · Base: CHF 298M · Bear: CHF 131M)

---

## Contents

### `/html/`
- **`gravitas-valuation-platform.html`** — Standalone single-file platform (334KB, offline-capable)
  - 16 dashboard sections with full bilingual DE/EN support
  - 10 interactive Chart.js visualizations (EV ranges, comparable multiples, waterfall, PUE, energy costs, NPV, sovereign radar, etc.)
  - Bull/Base/Bear scenario toggle — all KPIs update dynamically
  - Language toggle (DE/EN) — all labels, charts, and content switch live
  - Print-to-PDF support via `Ctrl+P` or browser print (A4, nav hidden, clean output)
  - Zero external dependencies — fully works offline via `file://` in any modern browser

**How to open:** Double-click the HTML file, or drag it into Chrome/Firefox/Safari. No server required.

### `/pdf/`
The PDF version can be generated from the HTML platform:
1. Open `html/gravitas-valuation-platform.html` in Chrome
2. Press `Ctrl+P` (Windows/Linux) or `Cmd+P` (Mac)
3. Select "Save as PDF" → A4, no margins → Save

> Note: No pre-generated PDF is included in this delivery. The HTML `@media print` stylesheet produces institutional-quality A4 output directly from the browser.

### `/research/`
- **`comparables-research.md`** — Phase 1A comparables research brief (DEE-17)  
  11 AI datacenter/infrastructure comparables across Swiss, European, and global markets
- **`comparable-research-full.md`** — Complete DEE-17 research document

### `/comparables/`
- **`gravitas-comparables.json`** — Structured JSON of 7 transaction comparables used in the valuation model, plus 2 additional benchmark comparables, and Gravitas reference parameters

### `/valuation-model/`
- **`gravitas-valuation-model.json`** — Complete structured valuation model (DEE-18) including:
  - Weighted scoring model (infrastructure, sovereignty, energy, market, financial, ESG dimensions)
  - Bull/Base/Bear scenario definitions and calculations
  - Premium/discount attribution framework (Sovereign Exit at 12.9× vs base 18×)
  - Sensitivity analysis matrix
  - Risk matrix with probability and impact assessments

### `/sources/`
- **`sovereign-premium-scores.json`** — Sovereign premium scoring data (DEE-19)
- **`source-validation-report.md`** — DEE-22 source validation report covering all 11 comparables with A/B/C/D confidence ratings, contradictions, and fallback documentation

### `/qa/`
- **`qa-report.md`** — Complete QA process documentation:
  - Final sign-off (DEE-23): All 8 pass criteria verified — APPROVED
  - Full checklist covering completeness, offline capability, data accuracy, bilingual quality, visualizations, design, and print output

### `/visualizations/`
All visualizations are embedded directly in the HTML platform. No standalone visualization files were produced for this project.

---

## Key Metrics

| Metric | Value |
|--------|-------|
| Probability-weighted EV | CHF 363M |
| Bull scenario EV | CHF 1,062M (48.26 MW × 22× EBITDA) |
| Base scenario EV | CHF 298M (16.58 MW × 18× EBITDA) |
| Bear scenario EV | CHF 131M (8.75 MW × 15× EBITDA) |
| Sovereign premium score | 87/100 |
| Infrastructure score | 82.7% (368/445 pts) |
| Adjusted EV multiple | 12.9× (Base) |
| Target PUE | 1.08 |
| Power cost | CHF 0.10/kWh (20-year PPA) |

---

## QA Status

| Check | Result |
|-------|--------|
| Offline open (file://) | ✅ PASS — Zero operational external dependencies |
| All 16 sections present | ✅ PASS |
| 10 Chart.js visualizations | ✅ PASS — All rendering with real data |
| Scenario toggle (Bull/Base/Bear) | ✅ PASS |
| Language toggle (DE/EN) | ✅ PASS |
| No external requests | ✅ PASS |
| Print/A4 output | ✅ PASS |
| Data accuracy | ✅ PASS — All arithmetic verified |

**QA verdict: APPROVED** (DEE-23, DEE-27 · 2026-05-21)

---

## Research Pipeline

| Phase | Issue | Description |
|-------|-------|-------------|
| 1A | DEE-17 | Comparable discovery — 11 AI datacenter/infrastructure comparables |
| 1B | DEE-18 | Valuation model design — weighted scoring, scenarios, NPV |
| 1C | DEE-19 | Strategic positioning — sovereign premium, narrative, exit logic |
| 1D | DEE-22 | Source validation — all comparable data verified |
| 2 | DEE-20 | Platform architecture — single-file HTML, design system, bilingual |
| 3 | DEE-21 | HTML platform build — all 16 sections, 10 visualizations, bilingual |
| 4 | DEE-23 | QA & validation — data accuracy, bilingual, cross-browser, PDF |
| 5 | DEE-24 | GitHub delivery — this repository |
