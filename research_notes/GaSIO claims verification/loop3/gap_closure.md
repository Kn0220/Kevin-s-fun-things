# Loop 3 — Gap closure (GaSIO / VCBG claims verification)

Date: 2026-10-21. Agent: loop-3 gap-closing agent. Budget used: 56 WebSearch calls; GitHub code search (MCP) + raw.githubusercontent.com for primary texts; Oxfam S3 not needed this loop.

**Channel log.** WebFetch/curl to every non-GitHub host attempted this loop returned proxy 403 / DNS failure (cdn.standards.iteh.ai, webstore.ansi.org, cfpub.epa.gov, ssmeco.com, ctc-n.org, healthdata.org, stateofglobalair.org). GitHub REST search (`gh api search/*`, `api.github.com/search/*`, `repos/{owner}/{repo}/contents`) is blocked for non-configured repos, **but** the GitHub MCP `search_code` / `search_repositories` tools work and `raw.githubusercontent.com` serves any public file → this was the only "opened" channel. Every citation below is tagged **(opened)** when the text was read from a downloaded file, or **(search extract)** when it comes from a WebSearch summary.

Downloaded primary files (scratchpad, for audit): `/tmp/claude-0/-home-user-Kevin-s-fun-things/206939fd-f22b-5d72-8316-eca6446ec6c9/scratchpad/dl/apro/` (Aprovecho ISO code), `.../dl/stoves4.csv` + `capture_catalog.py` (Clean Cooking Catalog scrape), `.../dl/owid/energy.csv`, `co2.csv`, `energy_codebook.csv` (OWID/EI/GCP), `.../dl/verra/*.csv` (Verra registry dumps), `.../dl/vcs/cpa08.json(.txt)` (LLM-generated derivative of KCM CPA-08 PD — see caveat).

---

## Target 1 — ISO/TR 19867-3: which thermal-efficiency value do the tiers apply to?

**Angles tried (query → result, level)**
1. WebSearch (extended) `"ISO/TR 19867-3" thermal efficiency tiers "char" credit ... which efficiency value` → iTeh/ANSI preview pages: tiers run <10 % (Tier 0) to ≥50 % (Tier 5); "use the lower bound of the 90 % confidence interval for thermal-efficiency tier assignment"; targets are "informative guidance … not normative". No char footnote visible in the extract. An Aprovecho report for Zhejiang Huiwenmei (ssmeco.com PDF) "presents thermal efficiency with and without an energy credit for the char" — the report could not be opened (proxy 403). (search extract, L2 for the tier table; basis not stated)
2. curl of the iTeh sample PDF, ANSI preview PDF, EPA ScienceHub download, ssmeco.com report → all proxy 403. **Null.**
3. GitHub MCP code search `"19867" "char" "thermal efficiency" tier` → `aprovechodotorg/Data-Processing-Software` (Aprovecho Research Center, GPL, contact sam@aprovecho.org). Files read via raw.githubusercontent.com **(opened)**:
   - `LEMS/LEMS_EnergyCalcs_ISO.py` v0.41 (© 2022 ARC): computes `eff_wo_char` = "thermal efficiency with no energy credit for remaining char" per **Clause 5.4.4 Formula 6** (`Q1/B/Qnet,af`), and `eff_w_char` = "thermal efficiency with energy credit for remaining char" per **Clause 5.4.5 Formula 7** (`Q1/(B·Qnet,af − C·Qnet,char)`), plus `char_energy_productivity` (5.4.6 Formula 8) and `char_mass_productivity` (5.4.7 Formula 9). Both efficiencies are phase-weighted (hp/mp/lp) and **both are assigned a tier** (`tier_eff_wo_char`, `tier_eff_w_char`) with identical cut-offs 10/20/30/40/50 %.
   - `LEMS/LEMS_ISOReport.py`: the ISO report template lists "Thermal Efficiency without char" **and** "Thermal Efficiency with char", each with its own "Tier Rating" column.
   - `Osprey Report script/generate_tables.py`: `get_tier()` applies the same thresholds to "Thermal Efficiency w/o char" and "Thermal Efficiency w char"; CO tiers ≤3.0/4.4/7.2/11.5/18.3 g/MJd; PM2.5 ≤5/62/218/481/1030 mg/MJd.
   - `Osprey Report script/iso_tiers_dump.txt` = a dump of ISO/TR 19867-3 Table 1: Tier 5 ≥50 % / CO ≤3,0 g/MJd / PM2,5 ≤5 mg/MJd / safety ≥95 / durability <10; Tier 4 ≥40 / ≤4,4 / ≤62 / ≥86 / <15; Tier 3 ≥30 / ≤7,2 / ≤218 / ≥77 / <20; Tier 2 ≥20 / ≤11,5 / ≤481 / ≥68 / <25; Tier 1 ≥10 / ≤18,3 / ≤1030 / ≥60 / <35; Tier 0 below.  (opened; L5 as a lab's transcription of an L2 table — matches the protocol's B4 "Tier 4 PM2.5 ≤62 mg/MJd")
4. GitHub code search `"Mimi Moto" "thermal efficiency"` / `"Mimi Moto" 50 efficiency` → `JavoJavo/ecotec-catalog-webscrapping/streamlit_app/stoves4.csv`, a Selenium scrape of catalog.cleancooking.org (474 rows) **(opened)**. Mimi Moto row: ISO **efficiency tier = 4**, CO tier 5, PM2.5 tier 4; ISO thermal efficiency **49.7 %** (n = 1, year 2021, pellets); legacy IWA/WBT efficiency 46.8 % (2015, pellets — the same 46.8 % that Engineering for Change attributes to CSU EECL). Price USD 40–65. The scraper stores the ISO value in a column it named `iso_eff_char_val`, but its own comment says "MISSING DATA SOURCE HERE" and the sibling `iso_eff_val` column is empty, so the with/without-char label of the Catalog field is **not** confirmed by this file. Other rows for calibration: Philips HD4012 38.4 % → Tier 3; Envirofit G-3300 39.8 % → Tier 3; Three Stone Fire 14.4 % → Tier 1. No GaSIO/CCS/VCBG entry; the only Vietnamese rows ("North Vietnam Rice Husk Gasifier", "South Vietnam High Efficiency Stove") carry no ISO data.
5. WebSearch (extended) `"ISO 19867" gasifier OR TLUD "thermal efficiency" "char" "energy credit" ...` → OSTI paper (forced primary-air retrofit, 2024): ISO 19867 defines two efficiencies; the with-char value subtracts the energy in the remaining char, so it is always ≥ the without-char value; "the WBT protocol and historical lab reports of 'thermal efficiency' generally use the with-char definition"; their retrofit gained 34 % (without char) vs 21 % (with char). Tryner et al. 2014 (Envirofit PDF): in natural-draft TLUDs "up to 60 % of the energy input as fuel can remain as char", max TE 42 %, "both thermal and overall efficiencies should be calculated". DBFZ Apeli pellet stove (Energies 2023;16(7):3278): 44.1 % at 1116 W → Tier 4 efficiency, Tier 4 PM2.5, Tier 5 CO; basis not stated. (search extracts, L3)
6. WebSearch `"Mimi Moto" "50%" ... Berkeley Air OR CSU` and `"Mimi Moto" "49.7"` → only the CCA investor page ("ISO Tier 5 test results for Thermal Efficiency (50 %), Tier 5 CO, Tier 4 PM2.5") and a retailer ("above 50 %"); no lab report, no char basis. (search extract, L5/L6)
7. WebSearch `"19867-3" "Table 1" ... char footnote` and `cleancooking.org catalog ... char ... definition` and the ESMAP Bangladesh "Overview of ISO Standard" → nothing on char basis. **Null (3rd null angle on the TR text itself).**

**Finding.** The TR's own text on the basis of Table 1 was not opened (3 nulls). What the opened evidence shows: (a) Aprovecho — the lab that wrote the de-facto reference implementation — treats the Table 1 efficiency thresholds as applicable to **either** value and reports a tier for both the §5.4.4 (no credit) and §5.4.5 (char-credited) efficiencies; i.e., a bare "Tier 5 efficiency" claim is ambiguous until the basis is stated. (b) For a stove that is *sold as a biochar producer* (GaSIO; cf. A1–A4), the two values diverge strongly: if a fraction f of fuel energy remains as char, eff_w_char = eff_wo_char / (1 − f); with f ≈ 0.4–0.6 (Tryner's TLUD range) a 35–45 % no-credit stove reports 60–85 % with credit. (c) Mimi Moto: the Catalog's 2021 ISO value is 49.7 %, and the Catalog assigns efficiency **Tier 4**, not the Tier 5 that CCA's investor page and the GaSIO Overview's "matches Mimi Moto" comparison assume; whether 49.7 % is no-credit or credited is not stated in any source found — for a forced-draft pellet stove that burns its char down (char_energy_productivity small) the two values should be close, but this is an inference, not a measurement.

**Effect on verdict (claim IDs).**
- **B1** (CREEC Tier 5 efficiency, Tier 4 PM2.5): stays *Plausible, needs proof* (0.45 → 0.40). New required disclosure: which efficiency (§5.4.4 or §5.4.5) CREEC tiered. If the Tier 5 rests on the char-credited value, the brochure should say so; the benchmark stove (Mimi Moto) sits at Tier 4 / 49.7 % in the Catalog.
- **B2** ("Hiệu suất tối đa 83,7 %"): *Overstated* as an uncredited cooking efficiency (best published no-credit ISO values ≈44–50 %). Loop-C hypothesis now concrete: 83.7 % is reachable **only** as a char-credited §5.4.5 figure (e.g., 45 % no-credit with ≈46 % of fuel energy left as char), or as a non-ISO metric. Confidence 0.75 that the number is not a §5.4.4 value.
- **B4** (Tier 4 PM2.5 ≤62 mg/MJd "không tạo ra chất độc hại"): table confirmed (opened dump); verdict *Risky wording* unchanged.
- **B8/B2 cross-check**: the 73–75 % and 83.7 % family of CCS efficiency numbers is consistent with char-credited or combustion-efficiency reporting, not with ISO §5.4.4.

---

## Target 2 — Patent 1-2020-00995 (and 2017 utility solution, 2020 Denmark)

**Angles tried**
1. WebSearch `"1-2020-00995"` → only unrelated court dockets (Jalisco "0995/2020", Colombia, Ukraine). **Null.**
2. WebSearch `"Nguyễn Hồng Long" "sáng chế" "khí hóa sinh khối" bằng độc quyền` → no match; hits are a different inventor (Nguyễn Gia Long, waste-to-electricity, Báo Pháp luật) and generic gasification papers. **Null.**
3. WebSearch `"giải pháp hữu ích" "bếp khí hóa" sinh khối 2017 ... CCS` → no CCS/Long record; only Lê Trường An (Nam Định) "bếp sinh học" patent 2015 (VietNamNet) and VNUF 2024 paper (21.9 % vs 16.8 %). **Null.**
4. WebSearch `"Nguyen Hong Long" Denmark patent OR brugsmodel ... 2020` → nothing; only Jens Dall Bentzen and Chinese CN utility models. **Null.**
5. WebSearch `"Phương pháp và thiết bị khí hóa sinh khối" sáng chế OR "công bố" 2023 ipvietnam` → no VN record; USPTO and a 2015 HCMC DOST rice-husk gasification patent landscape only. **Null.**
6. WebSearch `patents.google.com OR patentscope "Nguyễn Hồng Long" ... gasification` → no patent record. Did surface the **CTC-N solution page** (ctc-n.org/solutions/volumetric-continuous-biomass-gasification-technology-vcbg-...): lists "Patent for Biomass Gasification Method and Equipment" and "Patents for volumetric continuous biomass gasification equipment used in green tea drying and household kitchens"; a follow-up extract notes the page's "Certifications" heading is empty. (search extract; CCS-authored content → L6)
7. GitHub code search `"1-2020-00995" OR "khí hóa sinh khối" "sáng chế"` → 0 results.

**Finding.** No patent-office record, number, filing/grant date or IPC surfaced through any indexed channel; the only new text is CCS's own CTC-N listing, which repeats the three patent claims without numbers. **Unresolved after 6 angles; log as null.**

**Effect on verdict.** **G1** stays *Unverified* (L6 only), confidence 0.35. What CCS could send: the Bằng number(s) (1-00xxxxx / 2-000xxxx), the WIPO Publish VN record for application 1-2020-00995, and the DKPTO/Espacenet number for the 2020 Danish right.

---

## Target 3 — BEST end-of-project figures (500 MSMEs; 77,600 tCO2; 34,740 t biomass; CTC-N MSME figure)

**Angles tried**
1. WebSearch `"77,600" OR "77.600" tCO2 ... "34,740"` → none of the figures found; EEAS page gives *targets*: 50 % of agri-food MSEs adopt; 1.4 Mt biomass by 300 small + 2,200 micro enterprises; 2 MtCO2e. (search extract, L5)
2. WebSearch `"IMPACT IN NUMBERS" Oxfam Vietnam BEST ...` → impact sheet (switch-asia.eu/site/assets/files/4631/best_impact_sheet.pdf) surfaced but extract cuts off before any results; **BEST Final-Evaluation ToR (Feb 2025, ngocentre.org.vn)**: "150,000 tonnes of biomass are used as fuel for VCBG in the four provinces" and "reduction of 500,000 tonnes of CO2 equivalent", plus impact indicator "50 % of 2,000 targeted agri-food MSEs report improved business viability" — the extract cannot tell whether these are revised targets or achievements. (search extract, L5)
3. WebSearch (Vietnamese) `dự án BEST Oxfam ... "500" doanh nghiệp "tấn CO2" ... tổng kết 2025` → background only (4 provinces, 2020–2024; EU/Oxfam/CCS). **Null** for results.
4. WebSearch `"3,800" ... linkedin OR facebook` → null. Oxfam node/1219 extract: project "concluded with significant potential for scaling up" after "four years of building an ecosystem"; one source gives end date 30 Nov 2025. No numbers. **Null.**
5. WebSearch `ctc-n.org VCBG ... "MSMEs" ... adopted` → **CTC-N page: "Transferred clean technologies and sustainable production models to 500+ MSMEs"**; "Presented at Mekong Start-up 2022"; 2015 household model "won an award". (search extract; CCS-authored → L6; page dated ≥2022 by content)
6. GitHub code search `VCBG gasification Vietnam OR "GaSIO"` → 0.

**Finding.** The "IMPACT IN NUMBERS" figures (3,800 / 500 / 77,600 / 34,740) are not on any indexed page; their provenance remains unidentified. New: the project's own Feb-2025 evaluation ToR frames results around 150,000 t biomass and 500,000 tCO2e (status ambiguous), and CCS's CTC-N profile says **500+ MSMEs** — half the brochure's "1000+".

**Effect on verdict.** **E2** ("1000+ MSMEs transferred"): downgrade from *Needs proof* to **Contradicted (internal)** — CCS's CTC-N profile says 500+, the brochure says 1000+; neither is independently verified. Confidence 0.6. **C-group** (programme-level CO2): the 77,600 t figure cannot be tied to a source; the ToR's 500,000 tCO2e is 4× smaller than the EEAS target (2 Mt) and 6× larger than 77,600 — three incompatible programme totals now circulate. What CCS/Oxfam could send: the Feb-2025 final evaluation report and the impact-sheet PDF.

---

## Target 4 — CREEC test of GaSIO

**Angles tried**
1. WebSearch `CREEC Makerere "Vietnam" gasifier stove ISO 19867 ... "CCS" OR "GaSIO" OR "VCBG"` → only CREEC's Zimbabwe biogas-stove ISO work (WE4F), Strathmore note that CREEC runs "an ISO recognized laboratory", and CREEC's Quad 2 report (Lima tiers; 42 %/41 % TE). **Null for Vietnam.** (search extract, L5)
2. WebSearch (Vietnamese) `"ISO 19867" bếp khí hóa sinh khối "Việt Nam" ... CREEC "Tier 5"` → CCA sector-directory entry for CREEC; nothing Vietnamese. **Null.**
3. WebSearch `ccs.org.vn OR ccspin.org CREEC Uganda "ISO 19867" GaSIO` → nothing from CCS domains. **Null.**
4. Clean Cooking Catalog scrape (opened): no GaSIO / CCS / VCBG product; no CREEC-tested Vietnamese stove. (L5 mirror)

**Finding.** No public trace of a CREEC ISO 19867-1 report for GaSIO (3 nulls + Catalog absence). CREEC is credibly an ISO-capable lab.

**Effect on verdict.** **B1, B3, B4, B6** unchanged (B1 *Plausible, needs proof*; B3 *Risky wording* — note CREEC's own clients describe "ISO 19867-1 certification", so the "chứng nhận" wording is sector-wide loose usage, not unique to CCS). What CCS could send: the CREEC report (test dates, fuel, both efficiencies, 90 % CI).

---

## Target 5 — BEST cost-benefit analysis 2023 (roasting cost per kg tea)

**Angles tried**
1. WebSearch (Vietnamese) `Oxfam BEST VCBG "sao chè" chi phí ... đồng/kg chè khô` → **VCBG user manual** (switch-asia.eu/site/assets/files/4632/3__best_vcbg_user_manual_vnm.pdf): VCBG cuts tea-roasting fuel cost "khoảng **10–30 % so với củi, 70 % so với điện và 80 % so với gas**"; CCS ToR (17 Jul 2024): production cost ≈ USD 4/kW. No đồng/kg figure. (search extract; CCS/Oxfam → L6)
2. WebSearch `baothainguyen.vn "khí hóa sinh khối" sao chè tiết kiệm ...` → no Báo Thái Nguyên hit; Báo Lào Cai repeats "tiết kiệm tới 50 % so với than đá và 80 % so với gas hoặc dầu". **Null** for đồng/kg.
3. WebSearch `"cost-benefit" ... VCBG 2023 BEST ... "per kg" OR "VND"` → CBA report not indexed; **ADB SEADS** article: Tran Nam Cooperative's "gas and electricity bills have fallen by VND 15 million per month" after switching (anecdote). Oxfam 2023 marketing ToR: adoption "slowly progressing due to strong resistance". (search extract, L5)

**Finding.** The CBA PDF (switch-asia.eu .../8_1_best_vcbg_cost-benefit_analysis_report_2023_vnm.pdf) remains unopened and unsummarised anywhere indexed. The project's own manual gives the savings ladder 10–30 % (wood) / 70 % (electricity) / 80 % (gas).

**Effect on verdict.**
- **D2** (vs LPG): manual's 80 % matches Overview p.2 (80 %) and p.14 (77 %), not the Brochure's "15 % of LPG cost" (85 %) or Household flyer "5–10 lần" (80–90 %) → *Contradicted* confirmed; the project's canonical figure is 80 %.
- **D3** (vs electricity): manual says 70 % saving; Brochure "rẻ hơn 10 lần" (90 %) and Green-tea flyer/Overview "50 %" both differ → *Contradicted* confirmed; 3.3× (70 %) sits between the two CCS claims and near loop-2's 3.1–7.7× tariff-based range.
- **D4** (vs wood): manual 10–30 % supports the Green-tea flyer (20 %) and the low end of the Household flyer (30–50 %); Brochure's "một nửa" (50 %) is the outlier → *Contradicted*, with the manual as the project's own lower benchmark.

---

## Target 6 — Vietnam fNRB (TOOL33 / A6.4) and KCM PoA 10477 / "VCS 2923"

**Angles tried**
1. WebSearch `"TOOL33" fNRB "Viet Nam" ... 36%` → background only (EB125 June 2025 approved national/regional defaults into TOOL33; TOOL30 withdrawn from 1 Jan 2026 — CCA statement). No country table. (search extract, L2/L5)
2. WebSearch (extended) `CDM "Information note" default fNRB values v03.0 ... "Viet Nam"` → **A6.4-MEP011-A04 and A6.4-MEP012-A04 (unfccc.int, draft A6.4 methodological tool): "Viet Nam 36" (%) in the national default table**; defaults "derived from the values listed in the CDM TOOL33 and based in substantial part on … Ghilardi & Bailis (2024)". Pakistan's 2025 value is 8 % (shows the spread). (search extract, **L2**)
3. WebSearch ×2 on KCM PoA 10477 CPAs → CDM registry: PoA 10477 "Viet Nam Improved Cookstove Project by KCM", AMS-II.G v11, DOE EPIC; **CPA 007 Yen Bai: 31,865 tCO2e/yr**, crediting 15 Jan 2020–14 Jan 2030; Thanh Hoa CPAs 009/012/013: 51,880 t/yr each (1 Oct 2021–30 Sep 2031); fNRB sheets listed as appendices but not readable. (search extract, L4)
4. GitHub code search `"Viet Nam Improved Cookstove Project by KCM"` → two Verra registry dumps mirrored on GitHub, read via raw **(opened; L5 mirror of L4 registry data)**:
   - `HaroldRobson/VCC_ledger` partitions and `ShouTakanohashi/Data-Science-Project-1/Data-Raw/Registered_Projects.csv` (columns: ID, Name, Proponent, Type, Methodology, Status, Country, Estimated Annual Emission Reductions, Registration date, Crediting period):
     | VCS ID | KCM CPA | Est. annual ER (tCO2e) | Registered | Crediting |
     |---|---|---|---|---|
     | 2487 | CPA 001 Hoa Binh | 44,888 | 2022-08-04 | 2019-04-26 → 2029-04-25 |
     | 2489 | CPA 002 Hoa Binh | 37,643 | 2022-10-03 | 2019-06-27 → 2029-06-26 |
     | 2490 | CPA 003 Phu Tho | 46,339 | 2022-11-22 | 2019-06-27 → 2029-06-26 |
     | 2491 | CPA 004 Phu Tho | 45,952 | 2023-01-17 | 2019-06-28 → 2029-06-27 |
     | 2492 | CPA 005 Thai Nguyen | 45,650 | 2023-01-09 | 2019-06-21 → 2029-06-20 |
     | 2493 | CPA 006 Thai Nguyen | 44,314 | 2023-01-09 | 2019-06-28 → 2029-06-27 |
     | 2594 | CPA 007 Yen Bai | 43,664 | 2023-02-05 | 2020-01-18 → 2030-01-17 |
     | 2595 | CPA 008 Yen Bai | 43,470 | 2023-02-20 | 2020-01-18 → 2030-01-17 |
     | 2671/2672 | CPA 009/010 Thanh Hoa | 51,880 each | 2023-01-16 / 01-12 | 2021-10-18 → 2031-10-17 |
     | 2703/2704/2705 | CPA 011/012/013 Thanh Hoa | 51,880 each | (listed) | 2021-10-26/27 → |
     | 5037 | CPA 001 — CER conversion | 44,888 | — | 2018-12-06 |
     Other Vietnamese cookstove projects in the dump: VCS 2523 Bridge Carbon "high efficiency wood burning cookstoves" 590,000 t/yr; VCS 2548 SIPCO grouped ICS 52,083; VCS 3820 Quang Nam 161,687; VCS 3836 SIPCO Phase 2 56,635.
   - **VCS 2923 = "Grouped Projects for Viet Nam Cookstove Program." — proponent Sustainability Investment Promotion and Development JSC (SIPCO), methodology VMR0006, 61,065 tCO2e/yr, registered 2022-11-25, crediting 2022-01-07 → 2032-01-06.** It is **not** a KCM project; loop 2's "KCM PoA 10477 / VCS 2923" pairing is corrected.
   - Note the CDM–Verra mismatch for Yen Bai CPA 007: 31,865 (CDM registry, search extract) vs 43,664 (Verra dump, opened).
5. GitHub `charlie-ccw/FYP-LLMs-for-Automated-Generation-of-Long-Domain-Specific-Documents/.../VCS-PD (v4.1)_VN_CPA-08 (version 1.4) Clean.json` **(opened, but L6 — this is an LLM-*generated* project description produced from the real CPA-08 PD for a thesis; numbers may be copied or hallucinated)**: "distribute **26,000** energy-efficient ICS ('4G' stoves) … Van Chan, Tram Tau, Van Yen districts, Yen Bai"; "annual reduction of approximately **43,093 tCO2e**", 10-year fixed crediting 18 Jan 2020–14 Jan 2030; net-to-gross 0.95 (AMS-II.G ¶39); baseline three-stone fires; a Phu Tho passage says 28,000 ICS. No fNRB value in the text. Indicative per-stove: 43,093/26,000 ≈ **1.66 tCO2e/stove/yr** (registry 43,470/26,000 ≈ 1.67).

**Finding.** Vietnam's national fNRB default of **36 %** is now confirmed in two UNFCCC A6.4 draft tool texts (search extract, L2). KCM's Vietnamese AMS-II.G CPAs are each credited ≈38–52 ktCO2e/yr; the only stove count found (26,000 for Yen Bai CPA 008) is from an unreliable derivative, giving an *indicative* ≈1.7 tCO2e/stove/yr.

**Effect on verdict.** **C1**: the derived ≈2.1 t/stove/yr from loop 2 is replaced by an indicative ≈1.7 t/stove/yr (flagged L6) for a registered Vietnamese wood-stove programme at fNRB-era (TOOL30) assumptions; with the 36 % national default the figure would fall further. Overview's 1,027 kg/yr stays *Plausible/conservative*; Household flyer's 3–5 t/stove/yr stays *Overstated* (≈2–3× an actual Vietnamese programme, before the fNRB cut). **C2** (4.5–7.5 t): *Overstated* by the same yardstick unless the service stove displaces coal/LPG rather than wood. Loop-2 text referring to "VCS 2923" as KCM must be corrected to SIPCO/VMR0006.

---

## Target 7 — SoGA 2024 Vietnam deaths (total, household) and EI 2025 Vietnam CO2 / fossil share

**Angles tried**
1. WebSearch `"State of Global Air 2024" Vietnam deaths ... household` → WHO Viet Nam page: "at least 70 000 deaths each year are air pollution-related" citing SoGA 2024; UNDP/UNICEF/WHO June-2024 op-ed repeats 70,000 and "1.4 years" life lost; **ADB RKSI deck (Mar 2025) citing SoGA 2024: Vietnam 99,700 deaths (2021)**. Household-only Vietnam number: not given (only global 3.2 M for 2020 / 3.8 M for 2016). (search extract, L2/L5)
2. WebSearch `stateofglobalair.org Vietnam "household air pollution" ...` → same 70,000; Vietcetera 2021 cites older WHO ≈60,000; VNU presentation: 56,808 PM2.5-attributable premature deaths (2019). **Null** for household split.
3. WebSearch (Vietnamese) `... "hộ gia đình" tử vong 2021 "State of Global Air 2024"` → WHO VN (VN-language) repeats 70,000 and 8.1 M global (2021); **VOV: MoH deputy minister citing GBD 2023 — 94,837 premature deaths/yr in Vietnam**, air pollution the 3rd-ranked risk. No household split. (search extract)
4. WebSearch (extended) SoGA country breakdown → SoGA 2024 global split ≈58 % ambient PM2.5 / 38 % HAP / 6 % ozone (extract jumbled); SoGA 2025 global: 4.9 M ambient PM2.5, 2.8 M HAP, 0.47 M ozone. curl of soga-2024-report.pdf (healthdata.org) and soga-2025-report.pdf → 403. **Null for Vietnam HAP.**
5. WebSearch GBD 2021 HAP Lancet paper (Mar 2025) / IHME ASEAN Viet Nam fact sheet → paper exists (204 countries) but country table not in extract; IHME sheet ranks air pollution #3 risk for Viet Nam (2021 DALYs). **Null (3rd) for household figure.**
6. EI 2025: WebSearch → only secondary (Worldometers 430.8 Mt fossil CO2 2024, IEA/EDGAR basis; Enerdata coal 51 % of energy; CAT uses EI 2025 growth rates). Then **OWID datasets via raw.githubusercontent.com (opened)**: `owid/energy-data` codebook: `fossil_share_energy` = "% of total primary energy, substitution method", source **Energy Institute — Statistical Review of World Energy (2025)**. Vietnam rows: fossil share **2024 = 78.47 %**, 2023 = 78.61 %, 2022 = 74.69 %, 2021 = 77.84 %; primary energy 2024 = 1,476 TWh (coal 47.6 %, oil 26.7 %, gas 4.2 %). `owid/co2-data` (Global Carbon Budget, not EI): Vietnam fossil CO2 **2024 = 370.9 Mt** (coal 229.2, oil 84.0, gas 12.1, cement 44.5), 2023 = 347.4 Mt, 2021 = 314.2 Mt; incl. LUC 484.2 Mt (2024); total GHG 583.5 MtCO2e; 0.96 % of global CO2. (opened; L5 mirror of L2/L4 data)

**Finding.** Vietnam all-air-pollution deaths: ≥70,000 (WHO quoting SoGA 2024), 99,700 for 2021 (ADB quoting SoGA 2024), 94,837 (MoH quoting GBD 2023); the household-only GBD 2021 number for Vietnam was not obtained (3 nulls). Fossil share of primary energy 2024 = 78.5 % (EI 2025 via OWID, opened); fossil CO2 2024 = 371 Mt (GCP via OWID, opened); EI's own CO2 series was not obtained (do not quote an EI tonnage).

**Effect on verdict.** **F1**: "≈75 % fossil" **Confirmed** at L2-via-mirror (78.5 % in 2024, 74.7–78.6 % over 2021–24); "1.7 triệu tấn CO2/năm" **Wrong** by ≈220× (371 Mt fossil CO2 2024; 430.8 Mt on the IEA/EDGAR basis). **F4** ("60,000 ca tử vong … ô nhiễm không khí"): refine from *OK as worded* to **Outdated/understated** — WHO's current Vietnam figure is ≥70,000 (SoGA 2024) and 2021 SoGA/GBD estimates are 95–100 k; the flyer's number is the pre-2020 WHO estimate. **F3** (2 M HAP deaths "WHO"): still *Outdated*; latest global HAP figures are 3.2 M (WHO, 2020), 2.8 M (SoGA 2025, 2023 data).

---

## Target 8 — Raw rice-husk and sawdust prices 2025–26; TKV official coal price 2025

**Angles tried**
1. Rice husk — WebSearch `giá trấu 2025 OR 2026 đồng/kg ...` → only daily rice bulletins (cám 7,950–8,050 đ/kg on 26 Jun 2026; no trấu). **Null.**
2. Rice husk — `"giá trấu" An Giang OR Đồng Tháp ... 2025` → VnExpress (undated in extract; article id 3123588 ≈ 2015): husk/ash 12,000–15,000 đ/bao, up from 5,000 → 10,000–12,000 đ/bao (Phú Tân, An Giang). **Null for 2025–26.**
3. Rice husk — `"giá trấu" 2025 ... "củi trấu" OR "trấu ép"` → VnExpress (old, undated): 1.3 t husk at **400 đ/kg** makes 1 t husk briquette sold at **1,500 đ/kg** (Quảng Nam); briquette production cost 270 đ/kg. Lai Châu 9-month-2025 price table has no husk row. **Null for 2025–26 (3/3).**
4. Sawdust — `giá mùn cưa 2025 ...` ×2 and `"mùn cưa" giá ... viên nén` → Trang Vàng listings price "Liên hệ"; pellet spec 8 mm, 8–12 % moisture, 4,200–4,800 kcal/kg; briquettes 4,300–4,600 kcal/kg. **Null (3/3).**
5. TKV coal — `giá than TKV 2025 than cám 4b/5a/6a` ×3 → no 2025 price decision indexed. Data points: MOIT page (undated, QĐ 2959): than cám 1 = 2.6 M đ/t, than cục 5a.1 = 3.29 M đ/t, ex-VAT at TKV depots; another MOIT page (8 fines grades, undated): cám 1 ≈ 2.35 M đ/t; **CLH 2024 draft contract: than cám 5a.6 = 2,059,000 đ/t, priced per QĐ 1092/QĐ-TKV of 30 Jun 2023**; 2016 decision: cám 6b.6 = 1,025,000 đ/t. 2025 context: TKV sold ≈44 Mt (below plan), tiêu thụ "gặp nhiều khó khăn" (Oct–Nov 2025). (search extracts, L4/L5)

**Finding.** No 2025–26 raw husk or sawdust quotation and no 2025 TKV price decision is indexed; best dated anchor is coal ≈2.06 M đ/t (cám 5a.6, 2023–24 contract basis) and 2.35–2.6 M đ/t (cám 1).

**Effect on verdict.** **D1** (40 / 50 / 54 % vs coal): coal input cost ≈2.0–2.6 M đ/t (2023–24) unchanged from loop 2; the internal 40–54 % spread remains *Contradicted*; no 2025 refresh possible. **A4** (biomass input "4–5× cheaper than 8 M đ/t biochar"): husk at the old 400 đ/kg (≈0.4 M đ/t) would be 20× cheaper, not 4–5×; current prices unknown → verdict unchanged (*Wrong label*), input ratio still unsupported.

---

## Summary table

| Target | Resolved? | Best level | One-line finding |
|---|---|---|---|
| 1. ISO/TR 19867-3 efficiency basis | Partly (TR text not opened; practice resolved) | L5 (opened: Aprovecho code + Table 1 dump); L2 tiers (search extract) | Aprovecho's ISO implementation tiers **both** §5.4.4 (no credit) and §5.4.5 (char-credited) efficiencies with the same ≥50 % Tier 5 cut-off, so a tier claim is ambiguous without its basis; Catalog lists Mimi Moto at 49.7 % → efficiency **Tier 4**, not 5; 83.7 % only reachable as a char-credited value. |
| 2. Patent 1-2020-00995 | No (6 nulls) | L6 | No patent-office record indexed; CTC-N page repeats CCS's three patent claims without numbers. |
| 3. BEST results provenance | Partly | L5 (ToR, search extract); L6 (CTC-N) | "IMPACT IN NUMBERS" figures unsourced; Feb-2025 evaluation ToR frames 150,000 t biomass / 500,000 tCO2e; CTC-N (CCS) says **500+ MSMEs** vs brochure 1000+. |
| 4. CREEC + GaSIO | No (3 nulls + Catalog absence) | L5 | No public CREEC report or Catalog entry for GaSIO; CREEC is an ISO-capable lab. |
| 5. BEST CBA 2023 | No (report not found) | L6 (project manual, search extract) | VCBG manual: savings 10–30 % vs wood, 70 % vs electricity, 80 % vs gas; ADB anecdote VND 15 M/month. |
| 6. fNRB 36 % / KCM / VCS 2923 | Yes (fNRB), Partly (per-stove) | L2 (A6.4 drafts, search extract); L5 mirror of Verra registry (opened); L6 for stove count | Viet Nam national fNRB default **36 %** confirmed in A6.4-MEP011/012-A04; KCM Yen Bai CPA 007/008 = VCS 2594/2595 at 43,664/43,470 tCO2e/yr; **VCS 2923 is SIPCO's VMR0006 programme (61,065 t/yr), not KCM**; indicative ≈1.7 tCO2e/stove/yr (26,000 stoves, unreliable source). |
| 7. SoGA 2024 / EI 2025 Vietnam | Partly (totals yes; household no; EI fossil share yes; EI CO2 no) | L2 via OWID mirror (opened); L5 (search extracts) | Deaths: ≥70,000 (WHO/SoGA 2024), 99,700 for 2021 (ADB/SoGA), 94,837 (MoH/GBD 2023); household split not found. Fossil share 2024 = 78.5 % (EI 2025); fossil CO2 2024 = 371 Mt (GCP). |
| 8. Husk/sawdust 2025–26; TKV 2025 | No (3 nulls each) | L4/L5 (older anchors) | No 2025–26 husk/sawdust quotes; coal cám 5a.6 ≈ 2.06 M đ/t (QĐ 1092/QĐ-TKV 2023, 2024 contract), cám 1 ≈ 2.35–2.6 M đ/t. |

### Verdict changes to carry into the revision
- **B1** keep *Plausible, needs proof*; add the basis question (which efficiency was tiered) and note Mimi Moto = Catalog Tier 4 (49.7 %).
- **B2** keep *Overstated*; add: 83.7 % is physically reachable only as a char-credited (§5.4.5) or non-ISO metric.
- **E2** downgrade to *Contradicted (internal)*: 500+ (CTC-N, CCS) vs 1000+ (brochure).
- **F1** 75 % → *Confirmed* at 78.5 % (EI 2025 via OWID, opened); 1.7 Mt → *Wrong* (371 Mt).
- **F4** 60,000 → *Outdated/understated* (≥70,000 WHO/SoGA 2024; 95–100 k on 2021 GBD basis).
- **C1/C2** benchmark: indicative ≈1.7 tCO2e/stove/yr for a registered Vietnamese AMS-II.G programme (flag source quality); fNRB 36 % national default now L2.
- **Loop-2 correction:** "VCS 2923" ≠ KCM; it is SIPCO's "Grouped Projects for Viet Nam Cookstove Program" (VMR0006).
- **D2/D3/D4**: project manual's canonical savings (80 % gas / 70 % electricity / 10–30 % wood) become the internal reference against which the brochure outliers (85–90 %, 10×, 50 %) are judged.
