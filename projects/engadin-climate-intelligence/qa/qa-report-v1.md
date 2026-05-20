# QA-Bericht / QA Report
## Engadin Climate Intelligence 2026–2036

**Erstellt von / Prepared by:** QA Agent  
**Datum / Date:** 20. Mai 2026  
**Deliverables geprüft / Deliverables reviewed:**  
- `html/engadin-climate-intelligence-2026.html` (163 KB, 2.410 Zeilen)  
- `pdf/engadin-climate-intelligence-2026.pdf` (28 KB, 11 Inhaltsseiten)

---

## Gesamturteil / Overall Verdict

> **⛔ ABGELEHNT / REJECTED**  
> 2 kritische Defekte und 3 Hauptmängel verhindern die Lieferung. Korrekturen erforderlich, danach erneute QA.  
> 2 critical defects and 3 major issues prevent delivery. Corrections required, followed by re-QA.

---

## 1. Zweisprachigkeit / Bilingual Completeness

| # | Prüfpunkt / Checkpoint | Status | Befund / Finding |
|---|---|---|---|
| 1.1 | Alle Sektionen haben DE + EN Inhalt / All sections have DE + EN | ✅ PASS | 218 DE / 218 EN Elemente, vollständig gepaart |
| 1.2 | Sprach-Toggle schaltet gesamten Inhalt um / Language toggle switches ALL content | ✅ PASS | JS schaltet `[data-lang]` und `[data-de]/[data-en]` korrekt |
| 1.3 | Keine gemischten Absätze / No mixed-language paragraphs | ✅ PASS | Klare `data-lang` Trennung in allen Sektionen |
| 1.4 | Diagrammbeschriftungen zweisprachig / Chart labels bilingual | ✅ PASS | Alle SVG-Diagrammtitel und chart-source Elemente haben DE/EN |

---

## 2. Daten & Quellenintegrität / Data & Source Integrity

| # | Prüfpunkt / Checkpoint | Status | Befund / Finding |
|---|---|---|---|
| 2.1 | Hauptaussagen zitiert / Major claims cited | ✅ PASS | Alle statistischen Kernaussagen haben Quellangaben (MeteoSwiss, SLF, FOEN, GLAMOS, CH2018) |
| 2.2 | Quellenvalidierung aus DEE-6 berücksichtigt | ✅ PASS | Abschnitt 8.3 dokumentiert 18 bestätigt, 11 eingeschränkt, 2 korrigiert |
| 2.3 | CHF-Schätzungen als solche gekennzeichnet | ✅ PASS | CHF 80–150 Mio. überall mit `⚠ Schätzung`-Badge und Disclaimer |
| **2.4** | **Daten in Diagrammen ≙ Daten im Text / Chart data matches text** | **⚠ MAJOR** | **Pers-Gletscher Flächenangaben inkonsistent — siehe F-02 unten** |
| 2.5 | Unsicherheit explizit markiert / Uncertainty explicitly marked | ✅ PASS | Disclaimer-Callout in Methodik (Abschnitt 08) klar formuliert |
| 2.6 | Keine Widersprüche zwischen Sektionen (ausser F-02) | ✅ PASS | Temperatur-, Schnee- und Wasserabflussdaten intern konsistent |
| 2.7 | Roseg-Gletscher 1990 Wert: kleiner Unterschied Deckblatt vs. Tabelle | ⚠ MINOR | Deckblatt-SVG: 4,0 km²; Tabelle Abschnitt 04: 4,2 km² — beide ergeben −50% |

---

## 3. HTML-Bericht (Technisch) / HTML Report (Technical)

| # | Prüfpunkt / Checkpoint | Status | Befund / Finding |
|---|---|---|---|
| 3.1 | Vollständig offline lauffähig / Works fully offline | ✅ PASS | Keine externen Ressourcen (keine CDN, keine Webfonts) |
| 3.2 | Kein externer Ressourcenabruf / No external resource requests | ✅ PASS | Keine `<link>`, `<script src=...>` oder `<img src=http...>` Elemente |
| 3.3 | Gesamtes CSS eingebettet / All CSS embedded | ✅ PASS | Vollständiges Stylesheet im `<style>`-Block |
| 3.4 | Gesamtes JavaScript eingebettet / All JS embedded | ✅ PASS | Sprach-Toggle-Skript im `<script>`-Block, keine externe Abhängigkeit |
| 3.5 | Navigation und TOC funktionieren / Navigation and TOC work | ✅ PASS | Alle 9 Ankerlinks `#cover` bis `#appendix` korrekt verknüpft |
| 3.6 | Responsives Layout / Responsive layout | ✅ PASS | Media Queries für 768px und 900px vorhanden |
| 3.7 | Druckvorschau / Print styling | ✅ PASS | `@media print` versteckt Nav/Toggle, setzt Seitenumbrüche, definiert Seitenränder |
| 3.8 | Sprach-Toggle ohne Seitenneuladung / Language toggle without reload | ✅ PASS | Rein JavaScript-basiert, kein Page-Reload |
| **3.9** | **Bevorzugte Schriften ohne Embedding / Preferred fonts not embedded** | **⚠ MINOR** | **Archivo / JetBrains Mono nicht eingebettet (`@font-face`); Fallback auf Helvetica/Courier bei fehlenden Systemfonts** |

---

## 4. PDF-Version

| # | Prüfpunkt / Checkpoint | Status | Befund / Finding |
|---|---|---|---|
| **4.1** | **Inhalt entspricht HTML-Version / Content matches HTML** | **⚠ MAJOR** | **Pers-Gletscher Fehler aus HTML in PDF übernommen (F-02); Diagramme als Platzhaltertext** |
| **4.2** | **Seitenumbrüche logisch / Page breaks logical** | **❌ CRITICAL** | **11 leere Seiten am Ende (Seiten 12–22) — nur Footer-Text, kein Inhalt — F-01** |
| 4.3 | Seitenzahlen vorhanden / Page numbers present | ⚠ MAJOR | Seitenzahlen erscheinen nur auf den 11 leeren Seiten, NICHT auf Inhaltsseiten |
| 4.4 | Diagramme druckauflösungsgerecht / Charts render at print resolution | ⚠ MAJOR | SVG-Diagramme nicht im PDF gerendert; erscheinen als `[Diagramm X — vollständige Visualisierung im HTML-Bericht]` Platzhalter |
| 4.5 | Keine verwaisten Überschriften / No orphaned headers | ✅ PASS | Inhaltsseiten 3–11 zeigen saubere Sektionsstruktur |

---

## 5. Branding

| # | Prüfpunkt / Checkpoint | Status | Befund / Finding |
|---|---|---|---|
| 5.1 | mindset-IT Branding subtil (nur Footer/Wasserzeichen) | ✅ PASS | Logo nur im Footer (24×24px SVG), "Powered by mindset-IT UG" — kein prominenter Auftritt |
| 5.2 | Brand-Farben korrekt: Mint #94B49C, Dark Ink #0A0A0A, Paper White #F7F6F2 | ✅ PASS | CSS Custom Properties exakt: `--mint: #94B49C; --ink: #0A0A0A; --bg: #F7F6F2` |
| **5.3** | **Keine Verläufe / No gradients** | **⚠ MAJOR** | **Alle 8 SVG-Diagramme nutzen `linearGradient` als Hintergrund-Fill — F-03** |
| **5.4** | **Keine abgerundeten Ecken / No rounded corners** | **⚠ MAJOR** | **SVG-Rects verwenden `rx="8"` und `rx="4"` — F-03** |
| 5.5 | 2px Borders wo verwendet / 2px borders | ⚠ MINOR | `--border-ink: 2px solid` ✅, aber `.badge { border: 1.5px solid; }` — F-04 |

---

## 6. Barrierefreiheit / Accessibility

| # | Prüfpunkt / Checkpoint | Status | Befund / Finding |
|---|---|---|---|
| 6.1 | Semantische HTML-Struktur / Semantic HTML | ✅ PASS | Korrekte Überschriftenhierarchie H1→H2→H3→H4 durchgehend |
| 6.2 | Alt-Text auf Bilder/Diagramme / Alt text on images/charts | ❌ FAIL | 10 Daten-SVG-Elemente ohne `role="img"` oder `aria-label` — F-05 |
| 6.3 | Ausreichender Farbkontrast / Sufficient color contrast | ✅ PASS | Dark Ink #0A0A0A auf Paper White #F7F6F2 (≥15:1), Mint auf Dark Ink gut lesbar |
| 6.4 | Keyboard-navigierbar / Keyboard navigable | ✅ PASS | Alle Links und Toggle-Button nativ fokussierbar |

---

## 7. Vollständigkeit des Berichts / Report Completeness

| # | Prüfpunkt / Checkpoint | Status |
|---|---|---|
| 7.1 | Titelseite mit Projektname, Datum, Auftraggeber | ✅ PASS |
| 7.2 | Executive Summary eigenständig nutzbar | ✅ PASS |
| 7.3 | Methodik beschreibt Ansatz | ✅ PASS |
| 7.4 | Alle 9 Analysesektionen vorhanden | ✅ PASS |
| 7.5 | Mindestens 3 Szenarien (RCP2.6, RCP4.5, RCP8.5) | ✅ PASS |
| 7.6 | Risikobewertung mit Wahrscheinlichkeit und Auswirkung | ✅ PASS |
| 7.7 | Handlungsempfehlungen spezifisch und priorisiert | ✅ PASS |
| 7.8 | Quellenverzeichnis vollständig | ✅ PASS |
| 7.9 | Anhang vorhanden (8 Rohdatentabellen) | ✅ PASS |
| 7.10 | Keine Platzhalter oder TODO-Marker | ✅ PASS |

---

## Detailbefunde / Detailed Findings

### F-01 — CRITICAL: PDF hat 11 leere Seiten am Ende / PDF has 11 blank pages at end

**Schweregrad / Severity:** Kritisch / Critical — blockiert Lieferung  
**Fundstelle / Location:** `pdf/engadin-climate-intelligence-2026.pdf`, Seiten 12–22 (PDF-Viewer)  
**Beschreibung / Description:**  
Das PDF enthält 22 Seiten im Viewer: Seiten 1–11 haben Inhalt (Deckblatt + 9 Abschnitte), Seiten 12–22 sind vollständig leer mit Ausnahme der Footer-Zeile `"Powered by mindset-IT UG · Engadin Climate Intelligence 2026-2036 · Seite X von 11"`. Die Seitenzahlen im @page CSS-Counter erscheinen AUSSCHLIESSLICH auf diesen Leerseiten, nicht auf den Inhaltsseiten.  
The PDF contains 22 pages in the viewer: pages 1–11 have content, pages 12–22 are completely blank except for the footer `"Powered by mindset-IT UG · Engadin Climate Intelligence 2026-2036 · Seite X von 11"`. The @page CSS counter page numbers appear ONLY on these blank pages, not on content pages.

**Empfohlene Lösung / Fix:** PDF-Generierung überprüfen und korrigieren. Vermutliche Ursache: `@page @bottom-center` counter erzeugt Duplikat-Seiten. 11 Leerseiten entfernen, Seitennummerierung auf Inhaltsseiten sicherstellen.  
**Verantwortlich / Owner:** Frontend Engineer Agent ([DEE-12](/DEE/issues/DEE-12))

---

### F-02 — MAJOR: Pers-Gletscher 1990-Fläche inkonsistent / Pers glacier 1990 area inconsistent

**Schweregrad / Severity:** Schwerwiegend / Major — sachlicher Fehler  
**Fundstelle / Location:**  
- HTML Abschnitt 04, Gletschertabelle (Zeile ~1503): Pers 1990 = **3,8 km²**, 2025 = 2,0 km²  
- HTML Executive Summary (Zeile 528): Pers −48% **(4,8 → 2,5 km²)**  
- HTML Anhang A6 (Zeile 2342): Pers 1990 = **4,8 km²**  
- HTML Deckblatt SVG Diagramm (Kommentar Zeile 388): Pers 1990 = **4,8 km²**  
- PDF Seite 6 Gletschertabelle: Pers 1990 = **3,8 km²** (aus fehlerhafter HTML-Tabelle übernommen)

**Beschreibung / Description:**  
Die Gletschertabelle in Abschnitt 04 (Wasserressourcen) zeigt Pers 1990 = 3,8 km², was identisch mit dem Morteratsch-2025-Wert ist und wahrscheinlich ein Kopier-/Tippfehler ist. Der korrekte Wert laut Executive Summary, Anhang A6 und Deckblatt-SVG ist 4,8 km². Rechnerische Verifikation: (4,8 − 2,5) / 4,8 = 47,9% ≈ −48% ✓  
The glacier table in section 04 shows Pers 1990 = 3.8 km², which matches Morteratsch's 2025 value and is likely a copy/typo error. The correct value per Executive Summary, Appendix A6, and cover SVG is 4.8 km². Math check: (4.8 − 2.5) / 4.8 = 47.9% ≈ −48% ✓

**Empfohlene Lösung / Fix:**  
- HTML Abschnitt 04 Gletschertabelle korrigieren: Pers 1990 = 4,8 km², Pers 2025 = 2,5 km²  
- PDF neu generieren  
**Verantwortlich / Owner:** Frontend Engineer Agent ([DEE-12](/DEE/issues/DEE-12))

---

### F-03 — MAJOR: SVG-Diagramme verwenden Farbverläufe und abgerundete Ecken / SVG charts use gradients and rounded corners

**Schweregrad / Severity:** Schwerwiegend / Major — Branding-Verletzung  
**Fundstelle / Location:** Alle 10 SVG-Elemente (HTML Zeilen 328, 603, 727, 894, 1008, 1120, 1249, 1378, 1537, 1912)  
**Beschreibung / Description:**  
Brand-Spezifikation: „Keine Verläufe, keine abgerundeten Ecken". Alle 8 Daten-SVGs plus Cover-SVG verwenden:  
- `linearGradient` als Hintergrundfarbe der Chart-Rechtecke (z.B. `fill="url(#bgGrad)"`)  
- `rx="8"` und `rx="4"` auf SVG-Rechtecken (abgerundete Ecken)

Brand specification: "No gradients, no rounded corners." All 8 data SVGs and the cover SVG use linearGradient fills and rx="4"/rx="8" on chart background rects.

**Empfohlene Lösung / Fix:** SVG-Diagramm-Hintergründe auf flache Farben umstellen (z.B. `fill="#F7F6F2"` oder `fill="#ffffff"`); `rx` Werte auf 0 setzen oder entfernen.  
**Verantwortlich / Owner:** Frontend Engineer Agent ([DEE-12](/DEE/issues/DEE-12))

---

### F-04 — MINOR: Badge-Rahmen 1,5px statt 2px / Badge border 1.5px instead of 2px

**Schweregrad / Severity:** Gering / Minor  
**Fundstelle / Location:** HTML CSS, Zeile 216: `.badge { border: 1.5px solid; }`  
**Beschreibung / Description:** Brand-Spezifikation sagt „2px Borders wo verwendet". Badges verwenden 1,5px.  
Brand spec says "2px borders where used." Badges use 1.5px.  
**Empfohlene Lösung / Fix:** Ändern zu `border: 2px solid;`  
**Verantwortlich / Owner:** Frontend Engineer Agent ([DEE-12](/DEE/issues/DEE-12))

---

### F-05 — MINOR: SVG-Diagramme ohne Barrierefreiheitsattribute / SVG charts missing accessibility attributes

**Schweregrad / Severity:** Gering / Minor  
**Fundstelle / Location:** HTML Zeilen 328, 603, 727, 894, 1008, 1120, 1249, 1378, 1537, 1912 — alle `<svg>` Datenelemente  
**Beschreibung / Description:** Alle 10 `<svg>` Datendiagramme haben kein `role="img"` und kein `aria-label`. Nur das Footer-Logo hat `aria-label="mindset-IT logo"`. Diagramme sind für Screen-Reader nicht zugänglich.  
All 10 data `<svg>` charts lack `role="img"` and `aria-label`. Screen readers cannot interpret them.  
**Empfohlene Lösung / Fix:** Hinzufügen z.B. `role="img" aria-label="Diagramm 1 — Jahresmitteltemperatur Engadin 1990-2036"` zu jedem Daten-SVG.  
**Verantwortlich / Owner:** Frontend Engineer Agent ([DEE-12](/DEE/issues/DEE-12))

---

### F-06 — MINOR: Temperatur-Diagramm Projektionstitel mehrdeutig / Temperature chart projection labels ambiguous

**Schweregrad / Severity:** Gering / Minor  
**Fundstelle / Location:** HTML Zeilen 668–670 (Chart 1 SVG text labels)  
**Beschreibung / Description:** Die Projektionsmarker am rechten Rand lauten `RCP2.6: +3.0°C`, `RCP4.5: +3.6°C`, `RCP8.5: +4.3°C` mit +-Vorzeichen, während die Y-Achse absolute Temperaturen (0–5°C) zeigt. Das +-Präfix suggeriert Anomalienwerte, obwohl es sich um absolute Stationswerte handelt. Executive Summary nennt "+3,0°C über vorindustriellem Niveau" — eine andere Metrik.  
Chart projection markers use "+" prefix for what appear to be absolute temperature values, creating ambiguity. Executive Summary "+3.0°C" refers to national anomaly vs 1871-1900 baseline — a different metric.  
**Empfohlene Lösung / Fix:** Achsenbeschriftung oder Projektionstitel um Kontextangabe erweitern (z.B. „~3,0°C abs." oder Fußnotenhinweis auf Referenzperiode).  
**Verantwortlich / Owner:** Frontend Engineer Agent ([DEE-12](/DEE/issues/DEE-12))

---

## Zusammenfassung Bewertungen / Severity Summary

| Schweregrad / Severity | Anzahl / Count | Defekte / Issues |
|---|---|---|
| ❌ Kritisch / Critical | 1 | F-01: PDF Leerseiten |
| ⚠ Schwerwiegend / Major | 3 | F-02: Pers-Daten, F-03: SVG Gradienten/Ecken, PDF Seitenzahlen |
| ℹ Gering / Minor | 3 | F-04: Badge-Rand, F-05: SVG Barrierefreiheit, F-06: Temperaturlabel |

---

## Erforderliche Fixes nach Agent / Required Fixes by Agent

**Frontend Engineer Agent ([DEE-12](/DEE/issues/DEE-12)):**
- F-01: PDF Leerseiten entfernen, Seitenzahlen auf Inhaltsseiten  
- F-02: Pers-Gletscher Tabellenwert korrigieren (3,8 → 4,8 km² 1990; 2,0 → 2,5 km² 2025)  
- F-03: SVG-Gradienten durch Volltonfarben ersetzen; rx=0 setzen  
- F-04: Badge-Rand von 1,5px auf 2px  
- F-05: `role="img"` + `aria-label` auf alle Daten-SVGs  
- F-06: Temperatur-Chartlabels disambiguieren  

---

## Freigabebedingung / Approval Condition

Erneute QA nach Korrektur von F-01 und F-02 (kritisch/schwerwiegend). F-03 bis F-06 können parallel oder in Folgeversion korrigiert werden, sollten aber vor CEO-Abnahme adressiert sein.

Re-QA after F-01 and F-02 are fixed (critical/major). F-03 through F-06 may be fixed in parallel or follow-up, but should be addressed before CEO sign-off.