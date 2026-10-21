# Group B — Lab performance and specifications (loop 1)

Verifier: Group B agent. Date: 2026-10-21.

## Tool constraints in this run (read before judging the loops)
- **Egress proxy policy-denied almost every host** (403 on CONNECT): cleancooking.org, catalog.cleancooking.org, ccs.org.vn, ccspin.org, creec.or.ug, iso.org, who.int, aprovecho.org, engineeringforchange.org, mdpi.com, sciencedirect.com, springer.com, researchgate.net, pmc.ncbi.nlm.nih.gov, wikipedia.org, ngocentre.org.vn, vietnam.oxfam.org, switch-asia.eu, ctc-n.org, worldbioenergy.org, vjol.info.vn, webstore.ansi.org, sis.se, rise.esmap.org, moit.gov.vn, congthuong.vn, genk.vn, tietkiemnangluong.com.vn, linkedin.com. The **only** page fetched in full was the Oxfam VCBG brochure PDF on the Oxfam S3 bucket (text extracted with pdftotext).
- **Every other citation below is "(search extract)"** per protocol: the fact comes from the search engine's extract of the cited page, not from opening it.
- **The shared WebSearch budget for the turn (200 calls) ran out** after my 23rd query. 24 further planned queries were refused and are listed under "Gaps for loop 2 — queries not run". Where a loop could not be run, it is marked **NOT RUN (budget)**; I did **not** downgrade any claim to "Unverifiable" on the strength of an un-run loop.
- Figures from the earlier research pass (files in `../GaSIO market and competitor analysis/`) are reused only where they carry a source; they are marked "(prior pass, search extract)".

## Reference: ISO/TR 19867-3:2018 default tier table (used for B1–B4)
Source: Clean Cooking Alliance summary of the TR (search extract, L5; the TR itself is paywalled and iso.org was blocked). Values match those in the prior pass (CCA doc 626-1-1.pdf) and WHO's 2021 "Setting national voluntary performance targets" page (search extract, L2).

| Tier | Thermal efficiency | CO (g/MJd) | PM2.5 (mg/MJd) | Safety score | Durability score |
|---|---|---|---|---|---|
| 5 | ≥ 50 % | ≤ 3.0 | ≤ 5 | ≥ 95 | < 10 |
| 4 | ≥ 40 % | ≤ 4.4 | ≤ 62 | ≥ 86 | < 15 |
| 3 | ≥ 30 % | ≤ 7.2 | ≤ 218 | ≥ 77 | < 20 |
| 2 | ≥ 20 % | ≤ 11.5 | ≤ 481 | ≥ 68 | < 25 |
| 1 | ≥ 10 % | ≤ 18.3 | ≤ 1030 | ≥ 60 | < 35 |
| 0 | < 10 % | > 18.3 | > 1030 | < 60 | ≥ 35 |

Notes from the same extracts: Tier 5 PM2.5 and CO "align with the WHO Guidelines for indoor air quality: household fuel combustion"; the targets are "informative guidance, not normative requirements"; they apply to stoves "with maximum firepower of up to 10 kW"; ISO 19867-1 itself covers stoves "typically below 20 kW". SFS (Finnish standards store) lists ISO/TR 19867-3:2018 as **withdrawn with a newer edition** — the current edition and any changed thresholds were not retrievable (gap). Tier 2 and Tier 1 safety/durability values are from the prior pass and should be re-checked in loop 2.

---

### B1 — CREEC ISO 19867-1 test: Tier 5 efficiency/durability/safety/CO, Tier 4 PM2.5
**Quoted (VN):** "Bếp đã được kiểm định theo tiêu chuẩn ISO 19867-1:2018 tại CREEC (Uganda, ISO/IEC 17025): Tier 5 hiệu suất, độ bền, an toàn, CO; Tier 4 PM2.5" — Overview ("2. Giới thiệu GaSIO"), p.4 (paraphrase of the brochure's wording as recorded in PROTOCOL.md; exact sentence to be re-quoted in loop 2 from the PDF)
**Prior verdict:** Plausible, needs proof (matches Mimi Moto; report not public)
**Loop A (direct):**
- `CREEC Makerere ISO 19867-1 test CCS Vietnam gasifier stove` → nothing linking CCS/GaSIO to CREEC. Found: CREEC tested a Zimbabwean biogas stove (press says "first ... to receive ISO 19867-1 certification", we4f.org, L5/L6 search extract); CREEC Quad-2 report shows 42 %/41 % thermal efficiency, i.e. the kind of output CREEC produces (bioenergylists PDF, search extract, L4). CCA sector directory lists CCS (two entries) with "Lab or Field Testing" as expertise but no results (cleancooking.org, search extract, L5).
- `"GaSIO" bếp khí hóa ISO 19867 CREEC` (VN) → null; only standard-store pages.
- `bếp khí hóa sinh khối CCS Nguyễn Hồng Long kiểm định Uganda Tier 5 ISO 19867` (extended, VN) → null for Uganda/Tier 5 in Vietnamese press. But: (i) CCS's own page says the household stove was tested **Dec 2015 at TU Delft, max efficiency 67 %** and the industrial gasifier was "recognised by MOIT and DANIDA, Dec 2016, 75 %" (ccspin.org, search extract, L6); (ii) a LinkedIn profile "Hong Long Nguyen – EBG Science and Technology Company Ltd." mentions the **GaSIO stove line, "chứng nhận hiệu suất 50 %" and an emissions test** (linkedin.com, search extract, L6).
- `CREEC Uganda cookstove testing laboratory ISO 17025 accredited test reports list stoves tested Vietnam` (extended) → CREEC lab recognised by UNBS under ISO/IEC 17025 (2005 edition on older pages, 2017 on newer); "tested over 50 types/models"; clients GIZ, UpEnergy, atmosfair, WWF DRC; no public per-stove results list; **no mention of Vietnam** (creec.or.ug, cleancooking.org, search extracts, L5).
- `"GaSIO" stove OR bếp EBG Vietnam gasifier` → **UN CTC-N technology profile** of VCBG/CCS states: "a CREEC lab, which is ISO/IEC 17025:2017 recognized, evaluated the performance of GASIO household stoves"; "stove durability assessment ... from the Forestry University"; "biochar analysis ... from Hanoi University of Science and Technology"; patent granted in Vietnam; >500 MSMEs; 2015 Sustainable Future Award with TU Delft (ctc-n.org, search extract; company-supplied text hosted by UNEP/UNIDO CTCN → **L6**). Also a World Bioenergy Association member-news item "Where there's smoke there's a solution: GaSIO lights the way" (worldbioenergy.org, search extract, L6; not opened).
- `site:catalog.cleancooking.org CCS Vietnam OR GaSIO OR VCBG` → **no Catalog entry surfaced** for any CCS stove (null).
**Loop B (benchmark):**
- `Clean Cooking Catalog Mimi Moto ISO 19867 tier ...` → CCA investor page: Mimi Moto "ISO Tier 5 ... Thermal Efficiency (50 %), Tier 5 for CO, Tier 4 for PM2.5" (data as of May 2023) (cleancooking.org/?p=11063, search extract, L5). WHO Module 7: a stove is "clean for health" only if PM2.5 is Tier 4/5 **and** CO is Tier 5; WHO lists the Mimi Moto forced-air gasifier among clean biomass technologies (who.int, search extract, L2).
- `"Mimi Moto" stove "kW" firepower ...` → E4C lists 46.8 % efficiency and CO 0.154 g/MJd (engineeringforchange.org, search extract, L5) — i.e. Tier 4 efficiency on E4C's number vs Tier 5 on CCA's.
- `"ACE One" ... ISO 19867 tier` → ACE One: 41.5 % thermal efficiency, PM 101.1 mg/MJd, CO 0.82 g/MJd (E4C/Catalog values, search extract, L5) → Tier 4 efficiency, Tier 3 PM2.5, Tier 5 CO; CSU/Covair tests "IWA-ISO tier 3–4", safety 97/100 (manufacturer, L6).
- `highest thermal efficiency biomass cookstove ISO 19867-1 ... peer-reviewed` (extended) → Apeli forced-draft stove 44.1 % at 1,116 W, 38.0 % at 526 W (Energies 2023, 16(7):3278, search extract, L3) → Tier 4 efficiency, Tier 5 CO, Tier 4 PM2.5 (prior pass). Natural-draft pellet TLUD 53 % vs Oorja FD 32 % (review, search extract, L3). Kenya natural-draft pellet TLUD **65–73 %** under ISO 19867-1 — **Research Square preprint, not peer-reviewed**, basis (char credit?) unknown (search extract, L5 at best). WBA pellet-cookstove paper: one ISO 19867-1 pellet test at 49 % (prior pass, L5). KS 1814:2019 (Kenya) requires ≥ 45 % for forced-draft stoves (rise.esmap.org copy, search extract, L4) — a regulator's view of "demanding".
- **Benchmark conclusion:** the only commercially sold biomass stove with a documented Tier 5 efficiency **and** Tier 5 CO is the Mimi Moto (CCA, May 2023 data; E4C's own number would make it Tier 4 efficiency). Tier 5 PM2.5 (≤ 5 mg/MJd) has no documented solid-biomass example; Tier 4 is the realistic ceiling. GaSIO's claimed profile therefore equals the best published profile, not better.
**Loop C (adversarial):**
- Is there a reading that strengthens the claim? Yes, two: (i) the CTC-N profile and the LinkedIn text independently (both CCS-authored) assert a CREEC evaluation and "50 %" efficiency — so a CREEC report very probably exists and its headline efficiency is likely ≈ 50 %, i.e. **exactly at the Tier 5 threshold**; (ii) CREEC is a CCA Regional Testing and Knowledge Centre whose UNBS recognition means "test results are officially accepted" (cleancooking.org, search extract, L5), so a CREEC report is credible evidence if produced.
- Is there a reading that weakens it? (i) A result of ~50 % sits on the Tier 5/Tier 4 boundary; a small change in fuel (loose husk vs pellets) or char treatment moves it to Tier 4 (E4C's 46.8 % for Mimi Moto illustrates this). (ii) No Catalog entry exists although CREEC/RTKCs routinely publish there. (iii) The same CCS documents give three different efficiencies for the household stove (67 % Delft 2015; 50 % LinkedIn; 83.7 % Overview 2025) — see B2.
- Planned but **NOT RUN (budget):** `ctc-n.org VCBG CCS "GASIO" CREEC ...`, `"GaSIO lights the way" ...`, `"EBG Science and Technology" GaSIO ...`, `CREEC ... Vietnam 2024 OR 2025 ... "Tier 5"`, `biomass cookstove ISO 19867 "Tier 5" thermal efficiency AND "Tier 5" CO list ... Ecosafi Jet-Flame`.
**Best evidence level:** L6 for the claim itself (CCS-authored text on CTC-N/LinkedIn); L5 for CREEC's accreditation and the Mimi Moto benchmark; L2 for the tier definitions.
**New verdict:** Plausible
**Confidence:** 0.50 — two CCS-authored sources now corroborate that a CREEC test happened and imply ≈ 50 % efficiency (threshold value), the profile matches the best commercial stove, but no report, Catalog entry or third-party mention exists.
**Change vs prior:** refined — same verdict; added that the likely measured efficiency is ≈ 50 % (boundary), that the profile equals (not exceeds) Mimi Moto, and that CCS's own documents name three different efficiencies.
**What CCS could send to settle it:** the CREEC test report (number, date, fuel, number of replicates, 90 % confidence intervals, thermal efficiency with and without char credit, char energy efficiency, CO and PM2.5 in g/MJd and mg/MJd per phase, safety and durability score sheets), plus permission to list it in the Clean Cooking Catalog.
**Sources:** [CTC-N VCBG profile](https://www.ctc-n.org/solutions/volumetric-continuous-biomass-gasification-technology-vcbg-sustainable-solution-agri-food) (search extract) · [CCA Mimi Moto investor page](https://cleancooking.org/?p=11063) (search extract) · [WHO Module 7 defining clean](https://www.who.int/tools/clean-household-energy-solutions-toolkit/module-7-defining-clean) (search extract) · [CREEC ISO 17025 recognition](https://www.creec.or.ug/2161-2/) (search extract) · [CCA RTKC list](https://www.cleancookingalliance.org/technology-and-fuels/testing/centers.html) (search extract) · [CREEC Quad 2 report](https://www.estufas.bioenergylists.org/files/quad_2_stove.pdf) (search extract) · [ccspin.org household gasification page](https://ccspin.org/index.php/vi/hoa-t-a-ng/ca-ng-ngha-i/267-cong-ngh-1) (search extract) · [LinkedIn Hong Long Nguyen / EBG](https://www.linkedin.com/in/hong-long-nguyen-5b390615/) (search extract) · [E4C Mimi Moto](https://www.engineeringforchange.org/solutions/product/mimi-moto/) (search extract) · [E4C ACE-1](https://www.engineeringforchange.org/solutions/product/ace-1-ultra-clean-biomass-cookstove/) (search extract) · [Apeli, Energies 2023](https://www.mdpi.com/1996-1073/16/7/3278) (search extract) · [Kenya TLUD preprint](https://www.researchsquare.com/article/rs-198040/v1) (search extract) · [KS 1814:2019](https://rise.esmap.org/data/files/library/kenya/Clean%20Cooking/Kenya_Biomass%20stoves-Performance%20requirements-KS%201814_2019.pdf) (search extract) · [CCA sector directory: CCS](https://cleancooking.org/sector-directory/centre-for-creativity-and-sustainability-ccs/) (search extract) · [WBA member news: GaSIO](https://www.worldbioenergy.org/news/923/219/Where-there-s-smoke-there-s-a-solution-GaSIO-lights-the-way/) (search extract, not opened)

---

### B2 — "Hiệu suất tối đa của bếp dân sinh là 83,7%"
**Quoted (VN):** "Hiệu suất tối đa của bếp dân sinh là 83,7%" — Overview, p.1
**Prior verdict:** Overstated (ISO Tier 5 ≥ 50 %; best tested biomass stoves 44–53 %)
**Loop A (direct):**
- `"ccs.org.vn" OR "ccspin.org" bếp khí hóa hiệu suất 83,7%` → no page with 83.7 % surfaced. Instead, a **CCS/BEST ToR (ngocentre.org.vn, 17 Jul 2024)** and the **SWITCH-Asia BEST VCBG user manual** state: "hệ số chuyển đổi từ nhiên liệu ra syngas là 98%, hiệu suất nhiệt cho bếp dân sinh là 67%, cho lò hơi là 85%" (search extracts, L5 — EU-project documents written by CCS/Oxfam). A Vietnam Forestry University journal paper (2024) on a household gasifier stove measured **21.9 %** vs 16.8 % for a traditional stove (vjol.info.vn, search extract, L3 — different stove, Vietnamese design).
- `bếp khí hóa ... Nguyễn Hồng Long ...` (extended) → ccspin.org: household stove tested Dec 2015 at **TU Delft, maximum efficiency 67 %** (search extract, L6). Genk (19 Oct 2017): "startup Việt chế tạo bếp sạch hiệu suất cao nhất thế giới" — the press framing CCS has used since 2017 (search extract, L6; basis not stated in extract).
- Prior pass (search extract, L6): VnExpress science-initiative contest entry "Bếp dân sinh GaSIO" by Nguyễn Hồng Long restates 83.7 %.
- **Internal record of CCS efficiencies for the same household stove:** 67 % (Delft 2015, repeated in BEST documents 2024) → "50 %" (LinkedIn, EBG/GaSIO) → 83.7 % (Overview 2025). Three bases or three stoves; none labelled.
**Loop B (benchmark):**
- `highest thermal efficiency biomass cookstove ISO 19867-1 ... 2022–2025 ... peer-reviewed` (extended) → Apeli 44.1 % (Energies 2023, L3); FD1.2 pellet stove 42.03 % (L3); forced-draft stoves "30–35 %" in a review (L3); mini FD stove up to 47 % by WBT (EGU26 abstract, 2026, L5); natural-draft pellet TLUD 53 % (L3); Kenya natural-draft TLUD 65–73 % (preprint, basis unknown, L5). Mimi Moto 50 % (CCA) / 46.8 % (E4C). Indian Purti fan stove 44–45 %, Mpurti 46–48 % (WBT) (search extract, L3). Prior pass: Tryner et al. 2014/2015 highest TE 42 % with up to 60 % of fuel energy left in char for natural-draft TLUDs (L3); systematic review: gasifier stoves typically 30–50 % (L3); WBA ISO 19867-1 pellet test 49 % (L5).
- **Benchmark conclusion:** the peer-reviewed/lab ceiling for heat-to-pot thermal efficiency of biomass stoves is ~45–53 %; the single higher number (65–73 %) is an un-reviewed preprint. 83.7 % is 1.6–1.9× the credible ceiling.
**Loop C (adversarial — is there a protocol or metric under which 83.7 % is legitimate?):**
- `ISO 19867-1 "energy credit for char" ...` → extracts did not return the clause text. Prior pass (SIS preview / ISO OBP, search extract, L2): ISO 19867-1 reports thermal efficiency **with and without energy credit for char** and defines **char energy efficiency** separately; OSTI retrofit study: 34 % without char credit vs 21 % with — showing the basis changes the number a lot (L4).
- `gasifier cookstove "cold gas efficiency" OR "combustion efficiency" ...` → forced-draft TLUD **cold-gas efficiency 58.6 %** with thermal efficiency only 26.7 % (Springer J. Braz. Soc. Mech. Sci. Eng. 2023, search extract, L3); Kirch PhD (Adelaide 2019): CGE 33 → 73 % as primary air ×5 (L3/L4); hot-gas gasification efficiency 52 % for a TLUD (L3). So **cold-gas/hot-gas efficiencies of 50–75 % are documented; 84 % is high even for those**.
- **Arithmetic (L1).** Let η_pot = heat-to-pot efficiency on fuel fed, f_char = share of fuel energy left in char. (a) *Char-credited thermal efficiency* η_cc = η_pot/(1−f_char). For η_cc = 83.7 %: η_pot 50 % needs f_char = 40 % (≈ 23 % char mass yield at 17 MJ/kg fuel, 30 MJ/kg char); η_pot 45 % needs f_char = 46 %; η_pot 40 % needs 52 %. Char yields of 20–30 % by mass **are** typical for TLUD/char-making stoves (Tryner: up to 60 % of energy in char), so **83.7 % is numerically reachable as a WBT/ISO "with char credit" figure**. But η_cc is then the fraction of *released* combustion heat captured by the pot, and 84 % flame-to-pot transfer in an open-pot stove has no published precedent (reported maxima ~50–60 % with skirts). (b) *Overall (pot + char) energy efficiency* η_pot + f_char = 83.7 % is fully plausible (e.g. 50 % + 33.7 %, or 45 % + 38.7 %) and is a metric Tryner et al. recommend reporting; it is **not** a cooking efficiency and is not what ISO tiers rate. (c) The BEST documents' "98 % fuel-to-syngas conversion" is **inconsistent** with (a) or (b): if 98 % of fuel energy leaves as gas, f_char ≤ 2 % and the stove's overall efficiency ≈ its pot efficiency (≈ 50–67 %). (d) 83.7 % is close to CCS's own "85 % for boilers" — a heat-exchanger figure that may have migrated to the stove line.
- Planned but **NOT RUN (budget):** `"Natural-Draft Wood Pellets Gasifier ... Kenya" 65 % 73 % char credit published journal`; `ISO 19867-1 thermal efficiency "char" "credit" ... "with and without"`; `startup Việt bếp sạch "hiệu suất cao nhất thế giới" ... genk`; `TU Delft 2015 test ... 67 %`; `ISO 19867-1 cookstove efficiency "upper limit" ... heat transfer pot`.
**Best evidence level:** L1 (algebra above) + L3 (peer-reviewed benchmarks) + L2 (ISO definitions, via prior-pass extracts).
**New verdict:** Overstated (as a cooking/ISO thermal efficiency) and **Contradicted** by CCS's own 67 % (2015/2024) and 50 % (LinkedIn) figures for the same stove class.
**Confidence:** 0.80 — the peer-reviewed ceiling is ~50 %; the figure can only be defended as a char-credited or "pot + char" overall efficiency, which CCS does not say, and which conflicts with its 98 %-syngas statement.
**Change vs prior:** refined — kept Overstated; added "Contradicted" (three CCS figures) and identified the one legitimate reading (overall pot + char energy efficiency, or char-credited TE with ~40 % energy in char) under which 83.7 % could be a real measurement.
**What CCS could send to settle it:** the page of the CREEC (or Delft) report that defines the 83.7 % metric; thermal efficiency with and without char credit; char energy efficiency and char mass yield for the test fuel; the fuel used.
**Sources:** [BEST/CCS ToR Jul 2024](https://ngocentre.org.vn/files/20240717-jul-17-ccs-tor.pdf) (search extract) · [SWITCH-Asia BEST VCBG user manual (VN)](https://www.switch-asia.eu/site/assets/files/4632/3__best_vcbg_user_manual_vnm.pdf) (search extract) · [ccspin.org household gasification page](https://ccspin.org/index.php/vi/hoa-t-a-ng/ca-ng-ngha-i/267-cong-ngh-1) (search extract) · [Genk 2017](https://genk.vn/con-nho-startup-viet-che-tao-bep-sach-hieu-suat-cao-nhat-the-gioi-khong-ho-lai-vua-co-them-mot-cai-gi-do-dau-tien-tren-the-gioi-nua-20171019183316136.chn) (search extract) · [VNUF stove paper, VJOL 2024](https://vjol.info.vn/mt/article/view/106721) (search extract) · [Apeli, Energies 2023](https://www.mdpi.com/1996-1073/16/7/3278) (search extract) · [Kenya TLUD preprint](https://www.researchsquare.com/article/rs-198040/v1) (search extract) · [FD TLUD cold-gas efficiency, Springer 2023](https://link.springer.com/article/10.1007/s40430-023-04473-7) (search extract) · [Kirch PhD 2019](https://eres.library.adelaide.edu.au/dspace/bitstream/2440/120509/1/Kirch2019_PhD.pdf) (search extract) · [Modular stove, Energy Conversion & Mgmt X 2026](https://www.sciencedirect.com/science/article/pii/S2590174526001558) (search extract) · [Tryner et al. 2015](https://envirofit.org/wp-content/uploads/2016/06/2015-The-effect-of-fuel-type-etc_Tryner.pdf) (prior pass, search extract) · [ISO 19867-1 OBP](https://www.iso.org/obp/ui/#iso:std:iso:19867:-1:ed-1:v1:en) (prior pass, search extract) · [OSTI 2418490](https://www.osti.gov/servlets/purl/2418490) (prior pass, search extract) · [VnExpress contest entry "Bếp dân sinh GaSIO"](https://vnexpress.net/khoa-hoc-cong-nghe/cuoc-thi-sang-kien-khoa-hoc/san-pham/bep-dan-sinh-gasio-808) (prior pass, search extract)

---

### B3 — "Bếp đạt chứng nhận theo tiêu chuẩn ISO 19867-1:2018"
**Quoted (VN):** "Bếp đạt chứng nhận theo tiêu chuẩn ISO 19867-1:2018" — Brochure (page not numbered)
**Prior verdict:** Risky wording (ISO 19867-1 is a test method, not a certification)
**Loop A (direct):**
- `Clean Cooking Catalog "verified" ... certification scheme ... national standard body certify Tier` → iso.org abstract: ISO 19867-1:2018 "specifies laboratory measurement and evaluation methods for particulate and gaseous air pollutant emissions, energy efficiency, safety, and durability of cookstoves" — a **test method**; the tiers live in a separate **Technical Report** (ISO/TR 19867-3) "that provides a simplified way for non-experts ... to rank stove performance" (iso.org / PMC8855438, search extracts, L2/L3). ISO/DIS 19867-1 (revision) is in development (iso.org 89051, search extract, L2).
- CCS's own English-language material (CTC-N profile) says CREEC "evaluated the performance" — not "certified" (search extract, L6). The LinkedIn text uses "chứng nhận hiệu suất 50 %" (search extract, L6).
**Loop B (benchmark — does any certification scheme exist that could justify "certified"?):**
- `KEBS cookstove certification KS 1814 ...` → **KS 1814:2019** (Kenya) is a *performance requirements* standard that references KS ISO 19867-1 for methods and sets minima (≥ 45 % efficiency for forced-draft stoves; PM2.5/CO caps in Table 3) — products can be certified against KS 1814, **not against ISO 19867-1** (rise.esmap.org copy, search extract, L4). Ethiopia **ES 6085:2019** is an analogous national requirements standard (rise.esmap.org, search extract, L4). Uganda: CREEC's UNBS recognition means "test results are officially accepted" by the national standards body (cleancooking.org, search extract, L5) — acceptance of a report, not a product certificate. ISO TC 285 secretariat is KEBS (search extract, L2).
- Vietnam: `QCVN khí thải bếp đun sinh khối ... TCVN hiệu suất bếp` → **no QCVN or TCVN for household biomass stoves found**; QCVN 19:2024/BTNMT covers industrial emissions only (vea.mae.gov.vn, search extract, L4). Null result.
**Loop C (adversarial):**
- Loose usage is widespread: press on the Zimbabwean biogas stove tested at CREEC says it "earn[ed] ISO 19867-1 certification" (we4f.org, search extract, L6), so CCS's wording follows a common habit; a UNBS-recognised CREEC report *is* a formal conformity-assessment output (ISO/IEC 17025 test report). That makes "tested by an accredited lab to ISO 19867-1" defensible — but "đạt chứng nhận theo tiêu chuẩn" (achieved certification to the standard) still implies a pass/fail requirement that ISO 19867-1 does not contain.
- Planned but **NOT RUN (budget):** `ISO "does not perform certification" ISO 19867 ...`; `Clean Cooking Catalog performance data "verified" OR "self-reported" ...`; `Vietnam national standard TCVN improved cookstove ...`.
**Best evidence level:** L2 (ISO abstract) + L4 (KS 1814 as the model of a real certifiable requirements standard).
**New verdict:** Overstated (wording) — ISO 19867-1 has no pass/fail criteria and ISO issues no certificates; the defensible statement is "tested to ISO 19867-1:2018 by an ISO/IEC 17025-recognised laboratory (CREEC); results rated Tier 5/4 against ISO/TR 19867-3 voluntary targets".
**Confidence:** 0.85 — the nature of ISO 19867-1 is unambiguous from ISO's own abstract; the only uncertainty is whether CREEC/UNBS issued any document that uses the word "certificate".
**Change vs prior:** refined — "risky wording" mapped onto the protocol scale as Overstated; added that national requirement standards (KS 1814, ES 6085) are what "certification" would actually require, and none exists in Vietnam.
**What CCS could send to settle it:** the exact CREEC document (test report vs. any "certificate" issued under UNBS recognition) and its scope statement.
**Sources:** [ISO 19867-1:2018](https://www.iso.org/standard/66519.html) (search extract) · [ISO/DIS 19867-1 revision](https://www.iso.org/standard/89051.html) (search extract) · [PMC8855438 review of ISO framework](https://pmc.ncbi.nlm.nih.gov/articles/PMC8855438) (search extract) · [KS 1814:2019](https://rise.esmap.org/data/files/library/kenya/Clean%20Cooking/Kenya_Biomass%20stoves-Performance%20requirements-KS%201814_2019.pdf) (search extract) · [Ethiopia ES 6085:2019](https://rise.esmap.org/data/files/library/ethiopia/Clean%20Cooking/Ethiopia_ES%206085-2019%20Clean%20Cook%20Stove.pdf) (search extract) · [CREEC UNBS recognition](https://www.creec.or.ug/2161-2/) (search extract) · [WE4F Zimbabwe biogas stove](https://we4f.org/?p=17629) (search extract) · [QCVN 19:2024/BTNMT](https://vea.mae.gov.vn/Data/files/20210708%20QCVN%20Khi%20thai%20cong%20nghiep.pdf) (search extract)

---

### B4 — "Không tạo ra chất độc hại trong quá trình đốt"
**Quoted (VN):** "Không tạo ra chất độc hại trong quá trình đốt" — Overview, p.2. Same wording in the EU/Oxfam VCBG brochure: "Không tạo ra chất độc trong quá trình đốt, an toàn cho sức khỏe người sử dụng" and "Không phát thải carbon" (Oxfam brochure PDF, **fetched in full**, L5).
**Prior verdict:** Risky wording (Tier 4 PM2.5 ≤ 62 mg/MJd is low, not zero)
**Loop A (direct):**
- Oxfam VCBG brochure (fetched) → repeats the absolute claim; gives no emissions numbers; adds "Buồng phản ứng có áp suất âm, ngăn chặn rò rỉ khí độc ra ngoài" — i.e. CCS itself acknowledges the reactor holds **toxic gas (CO-rich syngas)** that must be kept from leaking. The claim is thus EU-project language (L5 as to who said it, L6 as to evidence).
- VN press (`Oxfam ... độ bền ...` query) → tea producers in Thái Nguyên quoted as "mức khói thải gần như bằng không" (vietnam.oxfam.org, search extract, L5 — anecdotal).
**Loop B (benchmark):**
- Tier table above: Tier 4 PM2.5 = **≤ 62 mg/MJd**, Tier 5 CO = **≤ 3.0 g/MJd**; Tier 5 PM2.5 = ≤ 5 mg/MJd is the level "aligned with WHO guidelines" (CCA, search extract, L5; WHO 2021 publication page, search extract, L2). ISO 19867-3 tiers were derived with the **WHO Performance Target (PT) single-zone kitchen model** (who.int PT model page, search extract, L2); Aprovecho: tier-equivalent emission limits move with ventilation (Tier 4 CO < 2.2 g/MJd at 10 ACH vs up to 7 g/MJd at 30 ACH) (aprovecho.org, search extract, L5).
- WHO Module 7: "clean for health" = PM2.5 Tier 4 or 5 **and** CO Tier 5 (who.int, search extract, L2). So a stove with GaSIO's claimed Tier 5 CO + Tier 4 PM2.5 would qualify as **WHO-clean**, like the Mimi Moto.
- Arithmetic (L1): at Tier 4's ceiling a household delivering 5 MJ/day to the pot may emit up to 310 mg PM2.5 and 15 g CO per day — low, not zero; CO is acutely toxic at any emission rate if ventilation fails.
- Vietnam limits: no QCVN/TCVN for small stoves found (see B3); QCVN 19:2024/BTNMT is industrial (search extract, L4).
- Field caveat (prior pass, L3): Mimi Moto in Rwandan homes measured Tier 3–4 for CO/PM, with refuelling spikes — lab tiers overstate in-home exposure.
**Loop C (adversarial):**
- Reading that makes it defensible: "không tạo ra chất độc hại" as shorthand for "meets the WHO-aligned clean threshold (Tier 5 CO, Tier 4 PM2.5)". That is a legitimate, strong claim if the CREEC result holds, and WHO itself labels such stoves "clean".
- Reading that makes it worse: gasification *by design* produces CO/H2/tars (the "khí độc" CCS's own brochure says it contains); a Tier 4 PM2.5 stove emits up to 12× the Tier 5 (WHO-guideline) level; and the Oxfam brochure pairs the claim with "Không phát thải carbon", which is also false in the literal sense (biogenic CO2 is emitted; only the net is ~neutral).
- Planned but **NOT RUN (budget):** `WHO 2021 "Setting national voluntary performance targets" Tier 5 ... 35 µg/m3 ... 7 mg/m3` (to pin the exact WHO linkage values); `Vietnam national standard TCVN improved cookstove ...`.
**Best evidence level:** L2 (WHO/ISO tier definitions) + L1 (CO is toxic; Tier 4 ≠ zero).
**New verdict:** Overstated — as an absolute statement it is false; the defensible version is "low-emission: Tier 5 CO and Tier 4 PM2.5, which WHO classifies as clean for health".
**Confidence:** 0.85 — the tier thresholds and WHO definition are standards-level; only the exact WHO linkage numbers (35 µg/m³, 7 mg/m³) were not re-confirmed this run.
**Change vs prior:** refined — "risky wording" → Overstated, with the WHO "clean for health" reading recorded as the honest reformulation; flagged that the same absolute wording appears in an EU-funded Oxfam brochure (so the fix is needed there too).
**What CCS could send to settle it:** CREEC CO and PM2.5 results in g/MJd and mg/MJd (high- and low-power phases, with and across refuelling events); any in-home monitoring.
**Sources:** [Oxfam VCBG brochure PDF](https://oi-files-cng-v2-prod.s3.eu-west-2.amazonaws.com/vietnam.oxfam.org/s3fs-public/file_attachments/Brochure%20VCBG%20-%20final.pdf) (fetched) · [CCA Voluntary Performance Targets](https://cleancooking.org/news/10-16-2018-voluntary-performance-targets/) (search extract) · [WHO: Setting national voluntary performance targets (2021)](https://www.who.int/publications/i/item/9789240023987) (search extract) · [WHO PT model](https://www.who.int/tools/performance-target-model) (search extract) · [WHO Module 7](https://www.who.int/tools/clean-household-energy-solutions-toolkit/module-7-defining-clean) (search extract) · [Aprovecho: air exchange and ISO tiers](https://aprovecho.org/indoor-air-quality/air-exchange-rates-and-the-iso-tiers-of-performance/) (search extract) · [Oxfam Định Hoá story](https://vietnam.oxfam.org/vi/node/451) (search extract) · [QCVN 19:2024/BTNMT](https://vea.mae.gov.vn/Data/files/20210708%20QCVN%20Khi%20thai%20cong%20nghiep.pdf) (search extract)

---

### B5 — Power range "Từ 1 đến 6 kW" vs "0,5 - 10 kW"
**Quoted (VN):** "Từ 1 đến 6 kW" — Overview, p.3; "0,5 - 10 kW" — Household flyer
**Prior verdict:** Contradicted
**Loop A (direct):**
- Oxfam VCBG brochure (fetched) → no kW figure for any stove. BEST ToR (ngocentre, Jan 2023) → cost "khoảng 4 USD/kW công suất" (search extract, L5) — implies CCS sizes stoves by kW but no range given. `ccs.org.vn ... công suất kW điện tiêu thụ quạt W` → no spec sheet surfaced (null; ccs.org.vn blocked). ccspin.org (search extract, L6): "14 household models and 5 industrial models since 2010" — so **different models with different ranges are possible**.
**Loop B (benchmark):**
- Scope statements: ISO 19867-1 covers stoves "typically below 20 kW"; ISO/TR 19867-3 targets apply "up to 10 kW" (search extracts, L2) — so 0.5–10 kW sits exactly at the top of the household-target scope.
- Comparable forced-draft stoves: Apeli 0.53–1.12 kW (Energies 2023, L3); BioLite CampStove 3.4 kW (lo)–5.5 kW (hi) (eepower.com, search extract, L6); Mimi Moto retail listing "20,000 BTU/h" ≈ 5.9 kW (sportsmanswarehouse.com, search extract, L6); E4C gives no kW for Mimi Moto/ACE/HomeStove. Typical household firepower in the literature is ~1–6 kW with turn-down ratios of 2–6 : 1.
- Arithmetic (L1) at 16 MJ/kg fuel: 0.5 kW = 0.11 kg/h; 1 kW = 0.23 kg/h; 6 kW = 1.35 kg/h; 10 kW = 2.25 kg/h (husk at 13 MJ/kg: 0.14–2.8 kg/h). A 20 : 1 turn-down (0.5–10 kW) in one gasifier chamber is implausible: a bed sized for 2.3 kg/h cannot sustain stable gasification at 0.11 kg/h; 6 : 1 (1–6 kW) is within reported practice.
**Loop C (adversarial):**
- The two ranges may describe **different products**: "0,5 - 10 kW" could be the span across the household *family* (small camping-size to large family stove, cf. the 3 kW camping unit and the 1–20 kW service stove), while "1–6 kW" is one model. That would reconcile them, but both documents label the range "bếp dân sinh".
- Planned but **NOT RUN (budget):** `"Mimi Moto" firepower kW "high power" "low power" ISO 19867 CSU ...` (to get a lab-measured forced-draft power range).
**Best evidence level:** L1 (fuel-rate arithmetic) + L2 (scope limits) + L3 (Apeli).
**New verdict:** Contradicted (internal); the 0.5–10 kW span is also Overstated as a single-stove turn-down.
**Confidence:** 0.75 — the inconsistency is on the face of the documents; residual doubt only because CCS has many models.
**Change vs prior:** refined — kept Contradicted; added that 20 : 1 turn-down is implausible for one gasifier and that 1–6 kW matches comparable stoves.
**What CCS could send to settle it:** the model list with rated min/max firepower (kW) and fuel feed rate (kg/h) for each household model; the CREEC high-/low-power firepower values.
**Sources:** [Oxfam VCBG brochure PDF](https://oi-files-cng-v2-prod.s3.eu-west-2.amazonaws.com/vietnam.oxfam.org/s3fs-public/file_attachments/Brochure%20VCBG%20-%20final.pdf) (fetched) · [BEST ToR Jan 2023 Đại Từ demo](https://ngocentre.org.vn/files/20230111-best-tor4-demo-dai-tu.pdf) (search extract) · [ISO/TR 19867-3 scope via CCA](https://cleancooking.org/news/10-16-2018-voluntary-performance-targets/) (search extract) · [ISO 19867-1 scope](https://www.iso.org/standard/66519.html) (search extract) · [Apeli, Energies 2023](https://www.mdpi.com/1996-1073/16/7/3278) (search extract) · [BioLite CampStove power](https://eepower.com/news/grill-boil-cook-and-charge-with-the-biolite-campstove/) (search extract) · [Mimi Moto retail listing](https://www.sportsmanswarehouse.com/sportsmans/Smokehouse-Products-Mimi-Moto-Pellet-Stove/productDetail/Camping/prod99999059399/cat100829) (search extract) · [ccspin.org household page](https://ccspin.org/index.php/vi/hoa-t-a-ng/ca-ng-ngha-i/267-cong-ngh-1) (search extract)

---

### B6 — "đun sôi 1 lít nước trong 2 phút"
**Quoted (VN):** "đun sôi 1 lít nước trong 2 phút" — Overview, p.3
**Prior verdict:** Plausible (≈ 2.6 kW into water)
**Loop A (direct):** No independent boil test of a CCS stove found in any query (Oxfam brochure fetched: none; VN press: none). Prior pass (search extract, L6): CCS 2016 R&D update says gas appears "within about 1 minute of lighting" for the continuous prototype. The camping flyer claims "2-min heat-up" (CCS, L6).
**Loop B (benchmark):**
- `Mimi Moto ... ACE One ... BioLite HomeStove boil time 1 liter` → BioLite HomeStove: 1 L in 5 min, 5 L in 18 min (manufacturer claim via digitaltrends/Wikipedia, search extract, L6); BioLite CampStove: 1 L in ~4.5 min at 3.4–5.5 kW (eepower/REI, search extract, L6); Mimi Moto retail: "1 gallon in less than 8 minutes" (search extract, L6); E4C: time-to-boil "unknown" for Mimi Moto and ACE One (L5). Belonio household continuous-flow rice-husk stove: 2 L in 14 min (prior pass, L5).
- Arithmetic (L1): 1 L from 25 → 100 °C = 314 kJ (335 kJ for 80 K); in 120 s that is **2.6–2.8 kW delivered to the water**. Required firepower: 5.2–5.6 kW at 50 % heat-transfer efficiency, 5.8–6.2 kW at 45 %, 6.5–7 kW at 40 %. Comparators: BioLite CampStove delivers ~1.2 kW to water (21–34 % of firepower); Mimi Moto's gallon claim is ~2.5 kW to water (≈ 42 % of 5.9 kW) — so **2.6 kW into water is matched only by the Mimi Moto at full power on a large batch**, and is ~2.2× BioLite.
**Loop C (adversarial):**
- Favourable reading: at the top of the 1–6 kW range with ≥ 45 % high-power heat-transfer efficiency, a pre-heated stove **can** do it; "sôi" may mean visible boil at ~95 °C (less energy) and starting water may be warmer than 25 °C. Unfavourable: gasifier start-up (ignition to clean flame) typically takes several minutes, so "2 phút" cannot include lighting; at 1 L the pot's thermal mass and the time to reach full power matter; if the stove's true max is 6 kW the claim needs ≥ 44–47 % instantaneous efficiency — the Tier 5 boundary.
- Planned but **NOT RUN (budget):** `forced draft gasifier cookstove "time to boil" "1 L" ... ISO 19867 WBT results firepower kW`.
**Best evidence level:** L1 (energy balance) + L6 (competitor claims).
**New verdict:** Plausible — only at maximum firepower (≥ 5.5 kW), with the stove already running, and with efficiency at the Tier 5 level; not from a cold start.
**Confidence:** 0.60 — the energy balance is exact; whether the stove sustains ~6 kW at ~45–50 % efficiency is unverified.
**Change vs prior:** refined — same verdict with explicit conditions (pre-heated, max power) and a competitor comparison (2× BioLite's rate, ≈ Mimi Moto's).
**What CCS could send to settle it:** CREEC high-power phase data (firepower, time to boil for the ISO pot volume, efficiency) or a video/log of a timed 1-L boil including ignition.
**Sources:** [BioLite CampStove power/boil](https://eepower.com/news/grill-boil-cook-and-charge-with-the-biolite-campstove/) (search extract) · [REI CampStove review](https://www.rei.com/blog/?p=4814) (search extract) · [BioLite HomeStove boil claim](https://www.digitaltrends.com/?p=1357598) (search extract) · [E4C BioLite HomeStove](https://www.engineeringforchange.org/solutions/product/biolite-homestove) (search extract) · [Mimi Moto retail listing](https://blog.onparticipe.fr/products/mimi-moto-pellet-cook-stove/206600826) (search extract) · [Belonio household CF rice-husk stove](https://stoves.bioenergylists.org/node/2962) (prior pass, search extract) · [CCS continuous-gasifier R&D 2016](http://www.ccspin.org/index.php/en/news-information/303-update-on-continuous-gasifier-r-d-progress) (prior pass, search extract)

---

### B7 — "Độ bền tối thiểu của bếp 25,2 tháng vận hành" (VNUF) vs "Tuổi thọ 10 năm"
**Quoted (VN):** "Độ bền tối thiểu của bếp 25,2 tháng vận hành" (components 31,5–55,7 tháng; Đại học Lâm nghiệp) — Overview, p.5; "Tuổi thọ 10 năm" — Green-tea flyer / Overview p.5
**Prior verdict:** Contradicted
**Loop A (direct):**
- `Đại học Lâm nghiệp đánh giá độ bền thiết bị khí hóa sinh khối VCBG Oxfam BEST sao chè` (extended) → **Oxfam ToR "Consultant to assess VCBG equipment durableness"** (vietnam.oxfam.org/vi/node/1095): BEST sought "một nhóm tư vấn/một đơn vị đánh giá độ bền của bếp khí hóa sinh khối VCBG" for green-tea processing; "Kết quả đánh giá sẽ giúp dự án lựa chọn phương án nâng cấp bếp khí hóa tối ưu nhất" (search extract, L5). **Confirms a durability study was commissioned**; consultant, method and results not in the extract.
- `"Đại học Lâm nghiệp" khí hóa sinh khối độ bền tháng vận hành ...` → no VNUF durability report surfaced (null). VNUF authors published a 2024 gasifier-stove design paper (VJOL; 21.9 % efficiency) — shows VNUF works on gasifier stoves but not durability (search extract, L3).
- CTC-N profile (search extract, L6): "stove durability assessment ... from the Forestry University" — CCS-authored corroboration of the attribution.
**Loop B (benchmark):**
- ISO durability: ISO/TR 19867-3 Tier 5 durability = **score < 10** on ISO 19867-1's lab durability procedure (CCA, search extract, L5); the scoring formula was not retrievable (`ISO 19867-1 durability test protocol tiers score ...` → only general descriptions; L2 text paywalled). The ISO durability metric is a **score**, not months — so "25,2 tháng" is not an ISO 19867-1 result and the household stove's "Tier 5 durability" (B1) is a different measurement from the tea-stove field study.
- Service-life benchmarks for comparable burners: **NOT RUN (budget)**. Prior pass (L6): CCS gives 5-yr life for the bamboo-shoot unit and 3-yr for the bánh chưng unit vs 10-yr for the tea unit.
**Loop C (adversarial):**
- Reconciliation hypothesis (L1 arithmetic): if "tháng vận hành" means **months of continuous (24 h/day) operation**, 25.2 months = ~18,400 operating hours; at a tea roaster's typical duty of 1,200–2,000 h/yr that is **9–15 calendar years**, which would make "10 năm" consistent with the VNUF figure. If instead it means calendar months in service, the two statements conflict (2.1 vs 10 years). The component figures (31.5–55.7 months) suggest the 25.2 months is the **weakest component's** life (e.g., burner head/grate), so "tuổi thọ 10 năm" may refer to the frame with periodic part replacement — common for industrial burners but then the flyer should say so.
- Planned but **NOT RUN (budget):** `"Consultant to assess VCBG equipment durableness" ... methodology months`; `"Forestry University" OR "Vietnam National University of Forestry" VCBG gasifier durability ...`; service-life/warranty benchmarks for small biomass burners.
**Best evidence level:** L5 (Oxfam ToR proves the study was commissioned) + L1 (hours arithmetic).
**New verdict:** Contradicted as worded — but **reconcilable** if 25.2 months denotes continuous-operation-equivalent time or the shortest-lived component; the 10-year figure remains unsupported by any shown test.
**Confidence:** 0.55 — the conflict is explicit, yet a plausible definitional reconciliation exists and the underlying VNUF report was not seen.
**Change vs prior:** refined — kept Contradicted; added the Oxfam ToR (study is real), the ISO score-vs-months distinction, and the hours-based reconciliation to test in loop 2.
**What CCS could send to settle it:** the VNUF durability report (method, duty cycle assumed, definition of "tháng vận hành", component list), the BEST consultant's deliverable, and warranty terms offered to tea households.
**Sources:** [Oxfam ToR: assess VCBG equipment durableness](https://vietnam.oxfam.org/vi/node/1095) (search extract) · [Oxfam ToR: VCBG stove & fuel price appraisal](https://vietnam.oxfam.org/vi/node/1149) (search extract) · [CTC-N VCBG profile](https://www.ctc-n.org/solutions/volumetric-continuous-biomass-gasification-technology-vcbg-sustainable-solution-agri-food) (search extract) · [VNUF stove paper, VJOL 2024](https://vjol.info.vn/mt/article/view/106721) (search extract) · [CCA tier summary (durability score)](https://cleancooking.org/news/10-16-2018-voluntary-performance-targets/) (search extract) · [Thái Nguyên extension centre: VCBG conference](https://khuyennong.thainguyen.gov.vn/tin-noi-bat/-/asset_publisher/9O6FRbLItG65/content/hoi-nghi-gioi-thieu-cong-nghe-vcbg-trong-san-xuat-che-bien-che?inheritRedirect=true) (search extract)

---

### B8 — Industrial efficiency "lên đến 73%" vs ~75 % (MOIT/DANIDA 2016)
**Quoted (VN):** "lên đến 73%" — Overview, p.1; ccspin.org: "Máy khí hóa công nghiệp của chúng tôi đã được Bộ Công Thương và Tổ chức Hợp tác Phát triển Đan Mạch (DANIDA) công nhận vào tháng 12 năm 2016 đạt được hiệu suất 75% và tiết kiệm tới 70% chi phí nhiên liệu so với than" (search extract)
**Prior verdict:** Contradicted (minor)
**Loop A (direct):**
- `CCS khí hóa sinh khối Bộ Công Thương DANIDA 2016 công nhận hiệu suất 75% ...` (extended) → the 75 % statement exists **only on CCS's own ccspin.org page** (search extract, L6). moit.gov.vn and congthuong.vn articles on biomass gasification (2020–2022) discuss BEST and policy but **do not mention a 2016 recognition or any efficiency figure** (search extracts, L4 as to absence). scp.gov.vn notes industrial gasification in Vietnam is not widely deployed (search extract, L4). **No MOIT decision, DANIDA report or test record found** (null).
- Prior pass (search extract, L6): ccs.org.vn VCBG page states industrial efficiency "up to ~73 %"; BEST user manual/ToR: "hiệu suất nhiệt ... cho lò hơi là 85 %" (search extract, L5) — a **third** CCS industrial figure.
**Loop B (benchmark):**
- Gasifier-burner heat-to-process efficiency: cold-gas efficiencies 50–75 % are documented for small gasifiers (Kirch 2019; Springer 2023, search extracts, L3); Belonio's 19 kW continuous rice-husk gasifier "63 % overall" (prior pass, L5); Vietnamese boiler makers market 85–90 % for fluidised-bed/grate boilers (prior pass, L6). So **73–75 % for a close-coupled gasifier-burner on a dryer/roaster is plausible**; 85 % would be a boiler-level figure.
**Loop C (adversarial):**
- 73 % vs 75 % may be (i) two different industrial models (CCS lists five), (ii) a conservative later rounding, or (iii) "lên đến" (up to) vs "đạt được" (achieved) in one test — a 2-point gap is within test-to-test variation. The real issue is not 73 vs 75 but that **neither is backed by a retrievable MOIT/DANIDA document** and a third figure (85 %) also circulates.
- Planned but **NOT RUN (budget):** `DANIDA Bộ Công Thương 2016 ... LCEE ...` (the Danish-funded "Low Carbon Transition in the Energy Efficiency Sector" programme, 2013–2017, is the likely vehicle — unverified), `CCS ... "73%" OR "75%" ... ccs.org.vn`.
**Best evidence level:** L6 (all figures are CCS statements); L3 for the plausibility band.
**New verdict:** Contradicted (minor) — and both numbers Unverified against any official record.
**Confidence:** 0.60 — the discrepancy is small and explainable, but the recognition itself could not be traced beyond CCS's page.
**Change vs prior:** refined — kept; added that the MOIT/DANIDA record was not found in MOIT/Công Thương coverage and that a third CCS figure (85 % boiler) exists.
**What CCS could send to settle it:** the MOIT/DANIDA recognition letter or test report (Dec 2016), stating the device, fuel, method and measured efficiency; a note on which device "73 %" refers to.
**Sources:** [ccspin.org household gasification page](https://ccspin.org/index.php/vi/hoa-t-a-ng/ca-ng-ngha-i/267-cong-ngh-1) (search extract) · [ccs.org.vn VCBG page](https://ccs.org.vn/cong-nghe-va-san-pham/chi-tiet/cong-nghe-khi-hoa-sinh-khoi-lien-tuc-theo-the-tich-vcbg) (prior pass, search extract) · [MOIT: Công nghệ khí hóa sinh khối](https://moit.gov.vn/phat-trien-ben-vung/cong-nghe-khi-hoa-sinh-khoi-giai-phap-nang-luong-ben-vung2.html) (search extract) · [Công Thương 2020](https://congthuong.vn/cong-nghe-khi-hoa-sinh-khoi-giai-phap-nang-luong-ben-vung-cho-che-bien-nong-san-147226.html) (search extract) · [Công Thương: nhân rộng ... chính sách](https://congthuong.vn/nhan-rong-cong-nghe-khi-hoa-sinh-khoi-trong-che-bien-nong-san-can-hoan-thien-chinh-sach-147845.html) (search extract) · [SCP: Công nghệ khí hóa sinh khối](https://scp.gov.vn/tin-tuc/t307/cong-nghe-khi-hoa-sinh-khoi.html) (search extract) · [BEST VCBG user manual](https://www.switch-asia.eu/site/assets/files/4632/3__best_vcbg_user_manual_vnm.pdf) (search extract) · [Belonio 19 kW CF gasifier](https://stoves.bioenergylists.org/node/1159) (prior pass, search extract)

---

### B9 — "Công suất ước tính: 0.63 kW/h", "Điện tiêu thụ quạt: 1.1kW/h", "65 Wh/h"
**Quoted (VN):** "Công suất ước tính: 0.63 kW/h"; "Điện tiêu thụ quạt: 1.1kW/h" — Overview, p.7 (bamboo-shoot unit); "65 Wh/h" — Overview, p.5 (green-tea unit)
**Prior verdict:** Wrong (unit error)
**Loop A (direct):**
- Oxfam VCBG brochure (fetched, L5) → no power or fan-electricity specification at all. `CCS ... sấy măng khô ... công suất quạt ...` and `VCBG bếp sao chè ... quạt điện tiêu thụ W ...` → **NOT RUN (budget)**; `ccs.org.vn ... công suất kW điện tiêu thụ quạt W` → no spec page surfaced (ccs.org.vn blocked). **No corrected spec found anywhere.**
**Loop B (benchmark, L1 unit analysis):**
- "kW/h" is dimensionally kW per hour (a rate of change of power), not power (kW) or energy (kWh). "0.63 kW/h" and "1.1 kW/h" are therefore **meaningless as written**; "65 Wh/h" reduces to 65 W (a valid quantity written clumsily).
- Sanity check of the intended values (L1): the same page claims 2.2 t CO2 saved per t of dried bamboo shoots vs coal; at ~2.4 t CO2/t coal and 25 MJ/kg that is ~23 GJ ≈ 6,400 kWh of heat per tonne of product — **~100 h at 63 kW but ~10,000 h at 0.63 kW**. Evaporating the ~9 t of water in fresh shoots per tonne of dried product (~23 GJ) gives the same answer. So the intended thermal rating is almost certainly **63 kW** (decimal slip), consistent with the ≥ 75 kW tea unit on the neighbouring page.
- Fan electricity: 65 W for a ≥ 75 kW tea unit (0.09 % of thermal) is plausible for a small blower; **1.1 kW** for a similar-size bamboo unit is 17× higher — plausible only as a blower *motor rating* (1.5 HP) or as **1.1 kWh per day/batch**; the two pages are mutually inconsistent whichever reading is chosen. Other CCS units give fans of 80 W, 150 W and 240 W (prior pass, L6), bracketing 65 W and far below 1.1 kW.
**Loop C (adversarial):**
- Could "kW/h" be a Vietnamese shorthand for kWh (consumption per hour)? For the fan, "1.1 kWh per hour" = 1.1 kW — still 17× the tea unit. For "công suất 0.63 kW/h" no reading rescues 0.63 as a dryer's heat rating (see sanity check). The notation is a recurrent CCS habit (also "65 Wh/h"), so the problem is editorial, but the 0.63 vs 63 ambiguity is material to any buyer.
**Best evidence level:** L1 (dimensional analysis and energy balance).
**New verdict:** Impossible (as written: non-physical unit; 0.63 kW cannot dry bamboo shoots at the stated CO2 saving) — intended values unknown; most likely 63 kW thermal and either 110 W or 1.1 kWh/day for the fan.
**Confidence:** 0.95 on the unit error; 0.6 on the "63 kW" reconstruction.
**Change vs prior:** refined — kept Wrong/Impossible; added the drying-energy check that pins the intended rating near 63 kW and the 17× fan inconsistency between the two units.
**What CCS could send to settle it:** rated thermal output (kW), fan motor rating (W) and daily electricity use (kWh/day) for each unit on a corrected spec sheet.
**Sources:** [Oxfam VCBG brochure PDF](https://oi-files-cng-v2-prod.s3.eu-west-2.amazonaws.com/vietnam.oxfam.org/s3fs-public/file_attachments/Brochure%20VCBG%20-%20final.pdf) (fetched; no spec) · prior-pass extraction of the Overview spec table (`../GaSIO market and competitor analysis/company_materials.md`)

---

## Summary table

| ID | Prior verdict | New verdict | Best level | Confidence | Changed? |
|---|---|---|---|---|---|
| B1 | Plausible, needs proof | Plausible (CREEC test corroborated by two CCS-authored sources; implied efficiency ≈ 50 % = Tier 5 boundary; profile equals Mimi Moto) | L6 claim / L5 benchmark / L2 tiers | 0.50 | refined |
| B2 | Overstated | Overstated as ISO/cooking efficiency **and Contradicted** by CCS's own 67 % and 50 %; legitimate only as "pot + char" overall or char-credited efficiency | L1 + L3 | 0.80 | refined |
| B3 | Risky wording | Overstated (wording): ISO 19867-1 is a test method; certification exists only against national requirement standards (KS 1814, ES 6085), none in Vietnam | L2 + L4 | 0.85 | refined |
| B4 | Risky wording | Overstated: not zero; defensible as "WHO-clean: Tier 5 CO + Tier 4 PM2.5"; same wording in Oxfam/EU brochure | L2 + L1 | 0.85 | refined |
| B5 | Contradicted | Contradicted (internal); 0.5–10 kW also implausible as one stove's turn-down | L1 + L2 + L3 | 0.75 | refined |
| B6 | Plausible | Plausible only at ≥ 5.5 kW, pre-heated, ~45–50 % efficiency; ≈ Mimi Moto, 2× BioLite | L1 + L6 | 0.60 | refined |
| B7 | Contradicted | Contradicted as worded; reconcilable if 25.2 months = continuous-operation hours or weakest component; study confirmed commissioned by Oxfam | L5 + L1 | 0.55 | refined |
| B8 | Contradicted (minor) | Contradicted (minor); both 73 % and 75 % unverified (no MOIT/DANIDA record found); third CCS figure 85 % | L6 / L3 band | 0.60 | refined |
| B9 | Wrong (unit error) | Impossible as written; intended ≈ 63 kW thermal; fan 65 W vs 1.1 kW inconsistent 17× | L1 | 0.95 | refined |

No verdict was overturned; all nine were refined with new evidence or explicit conditions.

## Cross-group notes
- **For Group A (A3):** CTC-N's CCS profile attributes the biochar analysis to "Hanoi University of Science and Technology" (HUST), while the Overview says USTH (University of Science and Technology of Hanoi) — two different universities. Worth asking which lab issued the 95 % fixed-carbon figure.
- **For Group G:** CTC-N profile also lists the patent and ">500 MSMEs over a decade" (vs brochure "1000+", Group E2).
- **For Group D/C:** the BEST documents' "67 % household / 85 % boiler / 98 % fuel-to-syngas" figures are the efficiency bases CCS has used in EU reporting; any fuel-saving or CO2 arithmetic should be checked against 50–67 %, not 83.7 %.

## Gaps for loop 2

### Queries planned but not run (search budget exhausted at 23 queries)
1. `ctc-n.org VCBG CCS Vietnam "GASIO" CREEC ISO/IEC 17025 ... Forestry University ... Hanoi University of Science and Technology biochar` — open the CTC-N page for the full CCS text and any dates/tier numbers.
2. `"GaSIO lights the way" World Bioenergy Association CCS Vietnam stove` — WBA member news: check for CREEC/tier/efficiency statements.
3. `"EBG Science and Technology" GaSIO stove ... Hong Long Nguyen efficiency 50% emissions test` — pin the "50 %" wording and whether EBG is CCS's commercial arm.
4. `CREEC Makerere stove test Vietnam 2024 OR 2025 gasifier "Tier 5" biochar continuous feed` — CREEC social-media/annual-report mention of a Vietnamese stove.
5. `biomass cookstove ISO 19867 "Tier 5" thermal efficiency AND "Tier 5" CO list ... Ecosafi Jet-Flame Clean Cooking Catalog 2024 2025` — complete the Tier 5/Tier 5 benchmark list (Ecosafi, SSM Jet-Flame, Prime, Envirofit).
6. `"Natural-Draft Wood Pellets Gasifier Compared to Charcoal Cookstoves in Kenya" ... 65% 73% ... char credit published journal` — is the 65–73 % preprint char-credited, and was it ever peer-reviewed?
7. `ISO 19867-1 thermal efficiency "char" "credit" ... "with and without"` — confirm which basis the ISO/TR 19867-3 efficiency tier uses (with or without char credit); this decides whether a char-making stove's "Tier 5" is on the same footing as Mimi Moto's.
8. `startup Việt bếp sạch "hiệu suất cao nhất thế giới" ... genk 2017` — basis of the 2017 "world's highest efficiency" press claim (Delft figure? which metric?).
9. `TU Delft 2015 test Vietnamese biomass gasifier stove CCS 67% ...` — any Delft publication or test sheet.
10. `ISO "does not perform certification" ISO 19867 cookstove "certified" ...` — ISO's own wording for B3.
11. `Clean Cooking Catalog performance data "verified" OR "self-reported" ...` — Catalog verification labels (B1/B3).
12. `WHO 2021 "Setting national voluntary performance targets" Tier 5 ... 35 µg/m3 ... 7 mg/m3` — exact WHO linkage values for B4.
13. `Vietnam national standard TCVN improved cookstove ... "bếp đun" OR "bếp cải tiến"` — any TCVN for stoves (B3/B4).
14. `"Mimi Moto" firepower kW "high power" "low power" ISO 19867 CSU ...` — lab firepower range for B5/B6.
15. `forced draft gasifier cookstove "time to boil" "1 L" ... ISO 19867 WBT results firepower kW` — peer-reviewed boil times for B6.
16. `"Consultant to assess VCBG equipment durableness" Oxfam ... methodology months` and `"Forestry University" ... VCBG gasifier durability ...` — who did the study, method, definition of "tháng vận hành" (B7).
17. `ISO 19867-1 durability test procedure ... scoring` — durability score formula (B1/B7).
18. `DANIDA Bộ Công Thương 2016 khí hóa sinh khối CCS ... LCEE` and `CCS ... "73%" OR "75%" ... ccs.org.vn` — official record of the 2016 recognition (B8).
19. `CCS khí hóa sinh khối sấy măng khô ... công suất quạt ...` and `VCBG bếp sao chè ... quạt điện tiêu thụ W ... 75 kW` — corrected specs (B9).
20. `switch-asia.eu BEST VCBG user manual "hiệu suất nhiệt" 67% 85% 98%` — open the manual to quote the efficiency definitions (B2/B8).
21. `ISO 19867-1 cookstove efficiency "upper limit" ... heat transfer pot open flame` — published heat-transfer ceilings (B2).

### Documents to obtain (blocked hosts; try from an unrestricted environment)
- CREEC test report for GaSIO (via CCS) — the single item that would move B1–B4 and B6 to Confirmed/Overstated with high confidence.
- ISO/TR 19867-3 current edition (SFS lists the 2018 edition as withdrawn) — check whether thresholds changed.
- BEST VCBG user manual and July-2024 CCS ToR PDFs (switch-asia.eu, ngocentre.org.vn) — for exact efficiency-definition wording.
- Oxfam ToR node/1095 (durability) and node/1149 (price appraisal) full text.
- VNUF durability report; MOIT/DANIDA Dec-2016 recognition document.
- Clean Cooking Catalog entries for Mimi Moto, ACE One, and any CCS stove (catalog.cleancooking.org blocked).

### Open analytical questions
- Which efficiency basis does the ISO/TR 19867-3 tier use for char-producing stoves (with or without char credit)? If "with credit", a char-making stove's Tier 5 is easier to reach than Mimi Moto's.
- Is the LinkedIn "50 %" the CREEC mean, and what is its confidence interval? A mean of 50.x % with a wide interval may not support "Tier 5" under ISO 19867-1's reporting rules.
- Does "tháng vận hành" in the VNUF study mean continuous-equivalent months (reconciles with 10 years) or calendar months (contradicts)?
