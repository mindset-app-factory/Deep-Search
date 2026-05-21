# Source Validation Report — Gravitas Comparables Research

**Validation Agent:** Quellenprüfer ([DEE-22](/DEE/issues/DEE-22))
**Research Brief Validated:** [DEE-17](/DEE/issues/DEE-17) — Phase 1A Comparables Research
**Validation Date:** 2026-05-21
**Total Comparables Reviewed:** 11 primary + 1 benchmark transaction (Aligned DC) + market context data
**Paid Databases:** PitchBook, CB Insights, S&P Capital IQ, Preqin — SOURCE UNAVAILABLE; public fallbacks used throughout

---

## Quality Rating Legend

- **A — Official/Primary**: Government data, SEC filings, company press releases, official investor announcements
- **B — Reputable Secondary**: Established financial media (DCD, TechCrunch, Bloomberg, CNBC), market data providers, cross-verified
- **C — Unverified/Single-Source**: Single source, paid market research firm without public methodology, estimated/projected figures
- **D — Questionable/Contradicted**: Actively contradicted by a more authoritative source

---

## 1. Green Datacenter AG (Swiss) — PASS ✓

**Overall Rating: A**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| Entry EV ~CHF 210M (InfraVia from Altice, 2017) | CONFIRMED — MarketScreener: InfraVia acquired green.ch AG and Green Datacenter AG from Altice N.V. for approximately CHF 210M (Dec 1, 2017; completed Feb 12, 2018) | A | MarketScreener/Franklin Paris/Altice |
| Exit ~€1B (IFM Investors, Oct 2025) | CONFIRMED — Transaction completed Oct 30, 2025. Exact EV not publicly disclosed; multiple sources cite "about €1 billion ($1.1B)." IFM raising ~CHF 1.6B debt post-acquisition. | B | IFM press release, DCD, Bloomberg, BeBeez |
| Return multiple ~4.5× over 7 years | LIKELY — CHF 210M→~€1B implies ~4.75× gross; 4.5× is conservative estimate | B | Derived from A-rated data |
| ~100MW+ capacity | CONFIRMED — ZW campus 40MW+; ZW4 adds 12MW (Jan 2026) | B | DCD, Green specs |
| PUE 1.19 (Zurich West campus) | CONFIRMED | B | DCD/DatacenterMap |
| Investors InfraVia/IFM | CONFIRMED | A | Official announcements |

**Contradictions:** None. **Note:** The ~€1B exit EV was not formally disclosed; cite as "approximately €1B."

---

## 2. Vantage Data Centers — ZRH2 Zurich (Swiss) — PASS ✓

**Overall Rating: A**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| CHF 370M investment | CONFIRMED | A | Vantage PR, BusinessWire (Apr 11, 2024) |
| 24MW critical IT capacity | CONFIRMED | A | Vantage PR |
| 64MW combined ZRH1+ZRH2 | CONFIRMED | A | Vantage PR |
| 226,000 sq ft / Glattfelden, 30km north Zurich | CONFIRMED | A | Vantage PR |
| Implied CHF 15.4M/MW | CONFIRMED (370M ÷ 24MW) | A | Derived |
| PUE not publicly disclosed | CONFIRMED — press release does not disclose | B | Vantage PR |

**Contradictions:** None. Clean dataset.

---

## 3. Lefdal Mine Datacenter (European) — PASS with note ⚠

**Overall Rating: A**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| ~€400M total transaction value (3i, Mar 2026) | CLARIFICATION NEEDED — 3i's own RNS: "approximately €300M" for majority stake. Pulse2 reports "€400M Investment." The €300M is 3i's equity check; €400M likely includes total investment framing with follow-on capex. | B | 3i press release, Investegate RNS |
| 37MW operational, 43MW contracted | CONFIRMED | A | 3i press release |
| Up to 200MW potential | CONFIRMED | A | 3i press release |
| Norwegian hydropower 100% renewable | CONFIRMED | A | 3i press release |
| Prior investors: Columbia Threadneedle, UBS (debt) | CONFIRMED | A | 3i press release |

**FLAG:** Cite as "3i investment ~€300M for majority stake; total investment framing ~€400M."

---

## 4. Northern Data Group (European) — PASS with note ⚠

**Overall Rating: B**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| ~€774M market cap (May 2026) | CONFIRMED — NB2 Frankfurt: 773.57M EUR | A | Frankfurt exchange / StockAnalysis |
| €80M revenue (2025; down 34% YoY) | CONFIRMED — Audited FY2025: EUR 80M vs EUR 121M prior year; -33.9% ≈ -34% | A | Northern Data audited annual report (Mar 18, 2026) |
| Rumble acquisition | CONFIRMED — Rumble secured 81.3% of Northern Data | A | Rumble/Northern Data official announcements |
| 250MW capacity, 24,000 GPUs | LIKELY CORRECT | B | Edison Group, Northern Data annual report |

**FLAG:** Research states "Rumble acquisition announced (2026)" — INCORRECT TIMING. Rumble announced acquisition in **November 2025**, not 2026. Exchange offer completed Apr 2026 with 81.3% secured.

---

## 5. Nscale / Stargate Norway (European) — PASS with flags ⚠

**Overall Rating: B**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| $2B Series C (Mar 2026) at $14.6B valuation | CONFIRMED | A | TechCrunch (Mar 9, 2026), SiliconANGLE |
| Aker as 50/50 JV partner, OpenAI participation | CONFIRMED | A | Nscale/Aker/OpenAI press release |
| 230MW initial / 100,000 NVIDIA GPUs | CONFIRMED (forward-looking) | B | Nscale PR, EnergyTech |
| 520MW expansion target | UNCERTAIN — forward-looking, not independently confirmed | C | Research brief only |
| ~$1B initial JV capital (50/50 with Aker) | FLAG — Nscale PR states "upwards of USD 250M in equity on 100% basis" for the 20MW initial phase. The $1B in research conflicts with this figure. | C | Contradicts Nscale PR |
| $1.4B term loan | UNVERIFIED — Not found in any public source. No primary source confirmed. | C | UNVERIFIED |

**Additions:** Nscale's $14.6B company valuation is notable context not mentioned in research. **Contradictions:** $1B JV capital vs $250M stated in Nscale's own announcement.

---

## 6. Scaleway (Iliad Group) / AION Consortium (European) — CORRECTION REQUIRED ❌

**Overall Rating: B — factual error**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| 200MW AION capacity (288,000 H100 equiv.) | CONFIRMED | A | Scaleway press release |
| ~5,000 existing GPUs since 2023 | CONFIRMED | B | Scaleway |
| **PUE 1.16 (DC5 Paris)** | **INCORRECT — Scaleway DC5's own monitoring page shows design target PUE of ~1.25. Portfolio average is 1.37. No Scaleway facility has a confirmed PUE of 1.16.** | **D** | **Contradicted by Scaleway DC5 monitoring site** |
| EU Commission €180M sovereign tender / SEAL-3 | PARTIAL — SEAL-3 confirmed; AION submitted as candidate but award NOT confirmed | C | Scaleway PR, EU Commission |
| NVIDIA DGX Cloud Lepton partner | CONFIRMED | A | Scaleway PR |

**CORRECTION REQUIRED:** Remove/correct "PUE 1.16 (DC5 Paris)." Verified DC5 PUE design target is 1.25. Use 1.25 or N/A.

---

## 7. Echelon Data Centres / Echelon Iberdrola Digital Infra (European) — PASS with update ⚠

**Overall Rating: A (funding), B (capacity)**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| €1.7B loan financing (Morgan Stanley, Feb 2026) | CONFIRMED — multiple primary sources | A | Irish Times, DCD, Echelon PR |
| €2B+ Iberdrola JV (Jul 2025) | CONFIRMED | A | Iberdrola press room |
| $1.11B total equity funding | LIKELY | B | Bisnow, Irish Times |
| 600MW+ operational/planning (Ireland & UK) | OUTDATED — Echelon Feb 2026: "eight campuses across Europe totalling 1.2 GW." Research uses pre-Spain/Italy figure. | B | Echelon PR (Feb 2026) |
| 144MW Spain / 230MW grid, 700MW+ Iberdrola connections | CONFIRMED | A | Iberdrola press room |

**FLAG:** Update total Echelon pipeline from "600MW+ Ireland/UK" to "1.2GW across Europe"; 400MW operational or under development as of early 2026.

---

## 8. CoreWeave (Global) — PASS ✓

**Overall Rating: A**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| IPO at ~$23B valuation (Mar 2025, Nasdaq CRWV) | CONFIRMED | A | Nasdaq, CoreWeave IR |
| $5.1B revenue 2025 (+170% YoY) | CONFIRMED — $5.13B, +168% YoY | A | CoreWeave 10-K |
| $2.1B Q1 2026 (+112% YoY) | CONFIRMED — $2.078B | A | CoreWeave Q1 2026 results |
| $99.4B contracted backlog | CONFIRMED as of Q1 2026 (Mar 31); yr-end 2025 was $66.8B | A | CoreWeave Q1 2026 |
| $8.5B DDTL 4.0 + $3.1B DDTL 5.0 | CONFIRMED | A | CoreWeave PR |
| $2B NVIDIA investment (Jan 2026 at $87.20/share) | UNVERIFIED — NVIDIA stake is real; specific amount/date/price not confirmed from public sources | C | UNVERIFIED |
| ~850MW active / 3.1GW contracted | LIKELY | B | CoreWeave communications |

---

## 9. Crusoe Energy Systems (Global) — PASS with note ⚠

**Overall Rating: A**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| $10B+ valuation, $1.375B Series E (Oct 2025) | CONFIRMED | A | Crusoe PR, GlobeNewswire |
| Mubadala + Valor co-lead | CONFIRMED | A | Crusoe PR |
| ~$3.9B total equity funding | CLARIFICATION — $3.9B is total capital raised (debt AND equity across 13 rounds), not equity-only | B | Tracxn |
| $480M Series D (Mar 2025, $2.8B val) | CONFIRMED — Crusoe's own Series E PR cites this | A | Crusoe Series E PR |
| 1.2GW Abilene TX, 1.8GW Wyoming | CONFIRMED | A | Crusoe newsroom |
| Revenue projections ($2B 2026, $5.5B 2028) | UNVERIFIED — internal forward projections | C | Unaudited |

**FLAG:** Label "$3.9B total equity" as "$3.9B total capital raised (debt and equity)" to avoid misrepresentation.

---

## 10. Lambda (Global) — PASS ✓

**Overall Rating: B**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| $1.5B Series E (Nov 2025), TWG Global | CONFIRMED | A | BusinessWire, TechCrunch, DCD |
| $4B–$5B valuation estimate | CONFIRMED AS ESTIMATE — Bloomberg reported; Lambda declined to confirm | B | Bloomberg |
| ~$760M ARR (2025) | ESTIMATED — Sacra private data | C | Sacra |
| $480M Series D (Feb 2025, $2.5B val) | LIKELY | B | DCD, TechCrunch |
| $1.5B NVIDIA GPU leaseback (18,000 GPUs, 4 years) | UNVERIFIED — not confirmed from primary sources | C | UNVERIFIED |

**FLAG:** Lambda NVIDIA GPU leaseback needs primary source before platform inclusion.

---

## 11. Nebius Group (Global) — CRITICAL CORRECTIONS REQUIRED ❌

**Overall Rating: A (public company) — two data errors**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| **~$25.6B market cap (May 2026)** | **INCORRECT — Actual NBIS market cap May 21, 2026 is ~$48-52B. Research is ~2× understated. The $25.6B reflects a pre-May 14 date (stock surged +32% on Q1 earnings released May 14, 2026; ATH $233.73).** | **D** | **Contradicted by Yahoo Finance/StockAnalysis (May 21, 2026)** |
| Meta $27B deal (5yr, Mar 2026) | CONFIRMED | A | CNBC (Mar 16, 2026), Motley Fool |
| Microsoft deal "$19.4B (5yr)" | CLARIFICATION — SEC Form 6-K: base contract is $17.4B through 2031; optionally up to $19.4B if Microsoft exercises additional options | B | Nebius SEC Form 6-K |
| $3B-$3.4B revenue guidance 2026 | CONFIRMED | B | Nebius investor comms |
| Q1 2026 revenue $399M, +684% YoY | CONFIRMED | A | Nebius Q1 2026 results (May 14, 2026) |

**CRITICAL CORRECTIONS:**
1. **Market cap**: Update from ~$25.6B to ~$48-52B (May 21, 2026).
2. **Microsoft deal**: Cite as "$17.4B base / up to $19.4B (options)" per SEC Form 6-K.

---

## 12. Applied Digital (APLD) (Global) — PASS with context ⚠

**Overall Rating: A**

| Claim | Verification | Rating | Source |
|---|---|---|---|
| ~$6.4B market cap (Dec 2025) | CONSISTENT — Current May 2026 cap ~$10-11B; Dec 2025 value of $6.4B fits trajectory | B | StockAnalysis |
| $2.35B senior secured notes (Nov 2025) | CONFIRMED — SEC 8-K; 9.25% coupon | A | SEC 8-K |
| ~$7B over 15-year CoreWeave lease (250MW) | CONTEXT REQUIRED — CoreWeave lease amended March 2026 (two data halls suspended); $7B projection may be reduced | B | Benzinga, 247WallSt |
| 600MW leased, 400MW Ellendale campus | LIKELY | B | Applied Digital PRs |

**CONTEXT FLAG:** CoreWeave lease amendment (March 2026) materially affects the $7B revenue projection.

---

## 13. Aligned Data Centers (Benchmark Transaction) — PASS ✓

**Overall Rating: A**

All material claims confirmed: $40B EV, BlackRock GIP + MGX + AIP consortium, 5GW platform, 50 campuses. Multiple independent primary sources. No contradictions.

---

## Market Context Data Points

| Data Point | Rating | Note |
|---|---|---|
| Global AI infra investment $202.3B (+75% YoY) | B | Crunchbase; plausible |
| Hyperscaler capex ~$700B (2026) | C | Analyst estimate only |
| Swiss DC colocation market $465M (2024) | C | Arizton (paid; SOURCE UNAVAILABLE methodology) |
| Swiss DC capacity ~851MW (2025) | C | Mordor Intelligence (paid; SOURCE UNAVAILABLE) |
| DC transaction volume $61B+ (2025 record) | B | Consistent with known deals |
| Norway 96% hydropower | A | National energy statistics |

---

## Consolidated Action List for Downstream Agents

### ❌ MUST CORRECT before build:
1. **Nebius market cap**: Update from ~$25.6B to ~$48-52B (May 21, 2026)
2. **Scaleway DC5 PUE**: Remove "1.16"; use 1.25 or N/A

### ⚠ MUST CLARIFY:
3. **Nebius Microsoft deal**: "$17.4B base / up to $19.4B (options)" — not "$19.4B" as stated
4. **Lefdal transaction**: 3i equity ~€300M; total investment framing ~€400M
5. **Nscale JV capital**: $250M equity for 20MW phase per Nscale PR; $1B figure in research not reconciled
6. **Echelon pipeline**: 1.2GW Europe-wide (not 600MW Ireland/UK)
7. **Northern Data Rumble timing**: Announced Nov 2025, not 2026

### 🔍 NEEDS PRIMARY SOURCE (flag for Research Agent):
8. Nscale $1.4B term loan
9. CoreWeave NVIDIA $2B investment (Jan 2026 at $87.20/share)
10. Lambda NVIDIA $1.5B GPU leaseback (18,000 GPUs)

### 📝 CONTEXT NOTES:
11. Crusoe $3.9B = total capital (debt + equity), not equity-only
12. Applied Digital CoreWeave lease amended March 2026; $7B projection may be reduced

---

## Final Source Quality Summary

| Comparable | Rating | Confidence |
|---|---|---|
| Green Datacenter AG | A | HIGH |
| Vantage ZRH2 | A | HIGH |
| Lefdal Mine DC | A | HIGH |
| Northern Data Group | B | HIGH |
| Nscale / Stargate Norway | B | MEDIUM |
| Scaleway / AION | B | MEDIUM — PUE correction required |
| Echelon + Iberdrola | A | HIGH |
| CoreWeave | A | HIGH |
| Crusoe Energy | A | HIGH |
| Lambda | B | MEDIUM |
| Nebius Group | A | HIGH (post-correction) |
| Applied Digital | A | HIGH |
| Aligned DC | A | HIGH |
