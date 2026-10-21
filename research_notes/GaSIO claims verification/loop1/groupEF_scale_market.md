# Loop 1 — Groups E and F (scale / track record; market and health figures)

Verifier: team agent (Groups E–F). Date: 2026-10-21.
Protocol: `../PROTOCOL.md` (evidence levels L1–L6, verdict scale, three-loop rule).

## Environment constraints that shaped this pass (read first)
- **Page fetches were blocked for every external host** in this session: the egress proxy answered `403` to CONNECT for who.int, switch-asia.eu, eeas.europa.eu, oxfam.org, moit.gov.vn, ngocentre.org.vn, ourworldindata.org, danviet.vn, gizenergy.org.vn, thanhtra.com.vn (status endpoint: `connect_rejected ... host is not allowed for this session`). Every citation below is therefore **(search extract)** — the figure comes from the search engine's quoted snippet of that page, not from my own read of the page. Loop 2 must open the primary pages.
- **The shared per-turn web-search budget (200 calls, all agents) ran out** after my 56th query. Twenty planned Loop-C / Vietnamese queries were refused and are logged under each claim as "NOT RUN (budget)" and collected in "Gaps for loop 2".
- All arithmetic (steam enthalpy, unit conversions, factor gaps) was recomputed locally (L1) — script output is reproduced inline.

---

### E1 — Boiler range "20 kg/h to 20 t/h steam" vs industrial range "300 kW – 3 MW"
**Quoted (VN):** "từ 20 kg hơi nước một giờ đến các lò có công suất 20 tấn hơi nước một giờ" — Boiler flyer; Overview p.13. Versus "300 kW - 3MW" — Overview p.6 (industrial).
**Prior verdict:** Contradicted (20 t/h ≈ 14.9 MW).

**Loop A (direct):**
- `"khí hóa sinh khối" lò hơi CCS Nguyễn Hồng Long` → only CCS/Oxfam ToRs on ngocentre.org.vn (2023 Đại Từ demo ToR; 2024 CCS ToR for tea-industry heat equipment), MOIT article, Tạp chí Công Thương explainer. **No boiler-size figure for any CCS/VCBG installation.** (L5/L6, search extract)
- `"Tre Xứ Thanh" khí hóa sinh khối lò hơi` and `"Tre Xứ Thanh" công ty tre luồng Thanh Hóa lò hơi sinh khối` → **null**: no page mentions a company "Tre Xứ Thanh"; Thanh Hóa bamboo-sector articles (Tạp chí Công Thương, VnEconomy) describe an unnamed processor installing a *fluidised-bed* biomass boiler, not a gasifier. (L5, search extract)
- `"Ngọc Động" Hà Nam khí hóa sinh khối lò hơi` → Báo Thanh tra, 23-02-2012: SPIN project (CCS's predecessor programme) with Công ty CP Nồi hơi Việt Nam tested a boiler fired by gasified spent mushroom substrate at Công ty Ngọc Động (Hà Nam); "thử nghiệm thành công". **Boiler capacity not stated in the extract.** (L5, search extract) [thanhtra.com.vn](https://thanhtra.com.vn/kinh-doanh-A08BE54D6/du-an-spin-buoc-dot-pha-cong-nghe-khi-hoa-F3FCD0EC.html)
- `SPIN "Ngọc Động" "Nồi hơi Việt Nam" khí hóa bịch nấm lò hơi tấn hơi 2012` → **null** for size; incidental benchmark: Vietnamese industrial boiler stock spans ~1–300 t/h (jst-ud.vn paper, L3, search extract).
- `Pisico Bình Định khí hóa sinh khối lò hơi` and `... "Pisico" năng lượng sinh khối khí hóa` → **null**. Pisico (Quy Nhơn, est. 1998) appears only as a wood-products exporter (yellowpages.vn, L6). The only Bình Định biomass energy story is Erex's 50 MW *stoker* power plant (COD 2030) — unrelated. (L5, search extract)
- `chè Quảng Bình Hà Giang khí hóa sinh khối lò hơi sao chè` → **null** for a "Quảng Bình" tea company in Hà Giang. Note: Hà Giang has a *Quang Bình* district (huyện Quang Bình), a tea area — the brochure name is probably that district, mis-spelled in the brief. Search with the correct spelling: **NOT RUN (budget)**.
- `Vipagro Vĩnh Phúc khí hóa sinh khối lò hơi CCS` and `Vipagro Vĩnh Phúc công ty nông sản lò hơi` → **null**: no page mentions "Vipagro". (search extract)
- `ccspin.org khí hóa sinh khối lò hơi tấn hơi` → ccspin.org not indexed in results; Clean Cooking Alliance directory lists CCS (Cầu Giấy, Hà Nội) as gasifier designer/trainer. **No t/h figure anywhere.** (L5/L6)
- `site:ccs.org.vn khí hóa sinh khối` → **NOT RUN (budget)**.

**Loop B (benchmark):**
- `saturated steam enthalpy 10 bar kJ/kg steam table` → GEMU saturated-steam pressure table: 10 bar(a), 179.9 °C, h_f = 763, h_fg = 2013, **h_g = 2776 kJ/kg**; Manipal worked example 2776.2 kJ/kg. (L1/L2, search extract) [gemu-group.com](https://www.gemu-group.com/gemu-cdn2/dokumente/42/bs_p_090_steam_pressure_table_water_en.pdf)
- `1 tấn hơi/giờ tương đương bao nhiêu kW` → no citable Vietnamese source; industry rule of thumb 1 t/h ≈ 0.65–0.7 MW (hot feedwater). (L6)
- Local L1 recomputation (feedwater 20 °C, h_f = 83.9 kJ/kg):

  | Steam P | Δh (kJ/kg) | 20 t/h → steam output | fuel input @ 80 % η | 20 kg/h → |
  |---|---|---|---|---|
  | 1 bar(a) | 2591 | 14.4 MW | 18.0 MW | 14.4 kW |
  | 8 bar(a) | 2684 | 14.9 MW | 18.6 MW | 14.9 kW |
  | 10 bar(a) | 2692 | **15.0 MW** | 18.7 MW | 15.0 kW |
  | 16 bar(a) | 2708 | 15.0 MW | 18.8 MW | 15.0 kW |
  | 10 bar(a), feed 105 °C | 2336 | 13.0 MW | 16.2 MW | 13.0 kW |

  Conversely, 300 kW ↔ 0.40 t/h and 3 MW ↔ 4.0 t/h steam (Δh = 2692).

**Loop C (adversarial):**
- Reading 1 — "20 t/h" is the *host boiler's* nameplate and the VCBG only supplies part of its heat: nothing in the flyer says so; even then "công suất 20 tấn hơi nước một giờ" is presented as the gasifier line's range.
- Reading 2 — the "300 kW–3 MW" line (Overview p.6) is a *different product* (process-heat VCBG) from the boiler line: possible, but the Boiler flyer and Overview p.13 are the same company's boiler offer, and no public installation anywhere near 13–15 MW (≈ 3 t/h+ biomass feed) was found.
- Reading 3 — typo "20 tấn" for "2 tấn": 2 t/h ≈ 1.5 MW would sit inside 300 kW–3 MW. Plausible but unsupported.
- Queries `"khí hóa sinh khối" "tấn hơi" ... 2024 2025` and `"Quang Bình" Hà Giang chè khí hóa sinh khối` → **NOT RUN (budget)**.
- Note the *lower* bound is also inconsistent: 20 kg/h ≈ 15 kW is 20× below 300 kW.

**Best evidence level:** L1 (steam enthalpy arithmetic; table values L2).
**New verdict:** Contradicted.
**Confidence:** 0.90 — the arithmetic is unarguable (20 t/h = 13–15 MW steam, 16–19 MW fuel input, i.e. 4–6× the 3 MW ceiling); the 0.10 covers the "two product lines / typo" readings, which CCS could clear up in one line.
**Change vs prior:** refined — same verdict; adds the feedwater/pressure sensitivity (13–15 MW), the 80 %-efficiency fuel-input view (16–19 MW), and the observation that the 20 kg/h floor is also 20× below the 300 kW floor. Also records that **none** of the five named boiler references (Tre Xứ Thanh, Ngọc Động, Pisico, Quang/Quảng Bình tea, Vipagro) could be found with a stated boiler size; only Ngọc Động (2012 SPIN test) exists in the press at all.
**What CCS could send to settle it:** reference list of boiler conversions with site, year, boiler nameplate (t/h, bar), gasifier thermal rating (kW) and biomass feed rate (kg/h); photos/commissioning reports for the largest unit; clarification whether "300 kW–3 MW" and "20 t/h" describe different product lines.
**Sources:** [Thanh tra 2012 SPIN/Ngọc Động](https://thanhtra.com.vn/kinh-doanh-A08BE54D6/du-an-spin-buoc-dot-pha-cong-nghe-khi-hoa-F3FCD0EC.html) (search extract); [GEMU steam table](https://www.gemu-group.com/gemu-cdn2/dokumente/42/bs_p_090_steam_pressure_table_water_en.pdf) (search extract); [CCS ToR Jul-2024](https://ngocentre.org.vn/files/20240717-jul-17-ccs-tor.pdf) (search extract); [BEST Đại Từ demo ToR 2023](https://ngocentre.org.vn/files/20230111-best-tor4-demo-dai-tu.pdf) (search extract); [jst-ud.vn boiler stock](https://jst-ud.vn/jst-ud/article/download/3188/3188/7014) (search extract); [CCA directory: CCS](https://cleancooking.org/sector-directory/centre-for-creativity-and-sustainability-ccs/) (search extract); [Tạp chí Công Thương, Thanh Hóa bamboo boilers](https://tapchicongthuong.vn/don-bay-khuyen-cong-quoc-gia--chap-canh-cho-nganh-che-bien-lam-san-thanh-hoa-but-pha-536460.htm) (search extract); [Erex Bình Định](https://mekongasean.vn/doanh-nghiep-nhat-ban-muon-dau-tu-2400-ty-dong-lam-dien-sinh-khoi-tai-binh-dinh-17342.html) (search extract).

---

### E2 — "1000+ MSMEs received clean technology"
**Quoted (VN):** "1000+ Các doanh nghiệp siêu nhỏ, nhỏ và vừa được chuyển giao các công nghệ sạch" — Brochure.
**Prior verdict:** Needs proof.

**Loop A (direct):**
- `SWITCH-Asia BEST project Vietnam biomass gasification results MSMEs final` → SWITCH-Asia impact sheet and project page, EEAS project page, and the **ToR for the BEST Final Evaluation (ngocentre, Feb 2025)**. All give *targets*: 2,500 agri-MSEs (300 small + 2,200 micro), 100 mechanical enterprises, 400 biomass suppliers; 1.4 Mt biomass used; 2 MtCO2e reduced; budget EUR 3,041,814 (EU 2,433,451); Oct 2020–Sep 2024, Thái Nguyên/Tuyên Quang/Yên Bái/Lào Cai. **No achieved-vs-target numbers, no unit count, no final evaluation report found.** (L5, search extract)
- `Oxfam Việt Nam dự án BEST khí hóa sinh khối doanh nghiệp kết quả` → Oxfam VN + MOIT pages; the "2.500 hộ chế biến nông sản, 100 doanh nghiệp cơ khí và 400 đơn vị cung ứng sinh khối" appear as target groups, and the 1.4 Mt / 2 MtCO2e as planned impacts. (L5, search extract)
- `khihoasinhkhoi.com VCBG dự án BEST kết quả số doanh nghiệp lắp đặt` → BEST app and demonstration events (Bảo Yên, Tuyên Quang); **no installed-unit count**. (L5/L6)
- `CCS Vietnam "1000" MSMEs clean technology transferred ccs.org.vn` → **null**; only ngocentre.org.vn consultancy postings (2021–2024) for BEST (standards for VCBG tea gasifier, 100 mechanical enterprises, etc.). The "1000+" figure appears **nowhere** outside the brochure. (L6)
- `World Vision Thường Xuân bếp khí hóa sinh khối 250`, `"Tầm nhìn Thế giới" "Thường Xuân" bếp khí hóa sinh khối 2025`, `World Vision Vietnam biomass gasification stoves Thanh Hoa Thuong Xuan 2025` → **null ×3**: no public trace of a 2025 World Vision / Thường Xuân stove distribution. (null result)
- `Báo Công Thương khí hóa sinh khối "chưa được nhân rộng"` and `congthuong.vn khí hóa sinh khối Oxfam CCS VCBG ... nhân rộng` → the exact phrase was not found; the nearest is the MOIT article (moit.gov.vn, BEST launch coverage) stating that biomass-energy models exist in Vietnam but **none has been widely applied**, blaming lack of affordable, locally-fit technology and support systems. (L4 — ministry website, search extract). Targeted congthuong.vn query → **NOT RUN (budget)**.
- `"Nguyễn Hồng Long" CCS ... đã chuyển giao hàng nghìn` and `hội thảo tổng kết dự án BEST ... 2024` → **NOT RUN (budget)**.

**Loop B (benchmark):**
- `BEST Oxfam VCBG final evaluation 2024 2025 results number of enterprises adopted` (extended) → Oxfam project page repeats 1.4 Mt biomass and 2 MtCO2e without labelling them as achieved; EU-delegation visit story (2022) says progress was **"behind schedule due to the Covid-19 pandemic coupled with people's hesitance to apply new technology"**; the BEST biochar market report (switch-asia.eu, 2024) says "thousands of enterprises implementing VCBG in this project will produce about 350,000 [unit cut off]" — a projection, not a count. (L5, search extract)
- Benchmark for Vietnamese gasifier-stove reach: SNV results-based-finance programme — Tiến Mạnh TLUD rice-husk stove sold **>5,000 units since June 2016** (snv.org, 2018). Shows four-digit household numbers are achievable, but households are not MSMEs. (L5, search extract)
- `BEST project mid-term review 2023 ... units` → **NOT RUN (budget)**.

**Loop C (adversarial):**
- Reading 1 — "1000+" counts *enterprises reached by any CCS programme since 2010* (SPIN 2010–2014, EEP Mekong, BEST, consultancy trainees): no cumulative public figure exists either way.
- Reading 2 — the brochure's "doanh nghiệp siêu nhỏ" includes the household-scale "hộ chế biến" of the 2,500 BEST target, so 1,000+ could be ~40 % of target achieved. Consistent with the "behind schedule" note, but **unsupported by any published number**.
- Reading 3 — the BEST final evaluation (commissioned Feb 2025) may contain the figure; it is not public.
- A wholly independent 2024–2026 deployment (World Vision 2025) could not be found at all.

**Best evidence level:** L5 (EU/SWITCH-Asia/Oxfam target documents; MOIT statement) — none bears on the achieved count.
**New verdict:** Unverifiable.
**Confidence:** 0.55 — three loops produced only targets (2,500) and a "behind schedule" note; the figure is plausible as a partial-achievement count but no independent document states it, and the only phrase found about scale-up says the model has not been widely applied.
**Change vs prior:** refined — "Needs proof" → Unverifiable, with the specific finding that the public record contains **targets only** (2,500 agri-MSEs / 100 mechanical / 400 suppliers; 1.4 Mt; 2 MtCO2e) and no achieved number, plus an EU note of delay.
**What CCS could send to settle it:** the BEST final evaluation report (2025) or Oxfam's final narrative report to the EU with the achieved MSE count and VCBG units installed; CCS's own cumulative installation register (site, province, year, product); World Vision 2025 handover documentation (Thường Xuân, 250 stoves).
**Sources:** [SWITCH-Asia BEST project page](https://www.switch-asia.eu/project/biomass-gasification-technology/) (search extract); [BEST impact sheet](https://www.switch-asia.eu/site/assets/files/4631/best_impact_sheet.pdf) (search extract); [EEAS BEST](https://www.eeas.europa.eu/projects-best_en) (search extract); [ToR BEST Final Evaluation, Feb 2025](https://ngocentre.org.vn/wp-content/uploads/2025/02/TOR-for-BEST-Final-Evaluation_Final.pdf) (search extract); [Oxfam VN BEST page](https://vietnam.oxfam.org/what-we-do-secured-livelihoods-and-resilient-communities/biomass-gasification-technology-sustainable) (search extract); [Oxfam: EU delegation visit, behind schedule](https://vietnam.oxfam.org/latest/image-story/delegation-european-union-eu-vietnam-visits-mechanical-and-biomass-processing) (search extract); [BEST biochar market report](https://www.switch-asia.eu/site/assets/files/4633/7_1_best_research_report_on_the_domestic_and_international_market_for_biochar_products_eng.pdf) (search extract); [MOIT article](https://moit.gov.vn/phat-trien-ben-vung/cong-nghe-khi-hoa-sinh-khoi-giai-phap-nang-luong-ben-vung2.html) (search extract); [SNV TM stove >5,000](https://snv.org/update/goodbye-coal-hello-rice-husks-replacing-coal-fired-stoves-biomass-cookstoves-vietnam) (search extract); [ngocentre CCS postings](https://ngocentre.org.vn/vi/node/66280) (search extract).

---

### F1 — "~75 % of fuel consumed in Vietnam is fossil, emitting over 1.7 million t CO2/yr"
**Quoted (VN):** "Gần 75% nhiên liệu tiêu thụ ở Việt Nam là nhiên liệu hóa thạch, thải ra trên 1,7 triệu tấn CO2/năm" — Overview p.2.
**Prior verdict:** 75 % Confirmed (EI 2024 ≈ 77 %); 1.7 Mt Wrong (actual ≈ 300–390 Mt).

**Loop A (direct):**
- `Vietnam CO2 emissions 2024 Energy Institute Statistical Review million tonnes` → Our World in Data (Global Carbon Budget): **371 Mt CO2 in 2024** (territorial fossil); Worldometers (EDGAR_2025/JRC-IEA): **390.7 Mt (2023), 430.8 Mt (2024)**; Climate Action Tracker uses EI growth rates. (L2/L4, search extract)
- `Energy Institute Statistical Review 2025 Vietnam CO2 emissions from energy 2024` (extended) → YCharts (source: Energy Institute): **374.56 Mt (2023) → 398.67 Mt (2024)**; statbase (citing the Review) 419.0 Mt (year unclear); EI 2025 global: 40.8 GtCO2e, +1 %. OECD Economic Survey Viet Nam 2025: emissions "even higher in 2024 owing to the rapid increase in the consumption of coal". (L2 via secondary, search extract)
- `"1,7 triệu tấn CO2" Việt Nam nhiên liệu hóa thạch` → **no source gives 1.7 Mt**. Nearest: VJOL paper — Vietnam **per-capita** CO2 rose from 0.36 t (1985) to **1.73 t (2010)**, and fossil share of energy consumption 29.6 % (1985) → 71.1 % (2011). (L3, search extract)
- `"1,7 triệu tấn CO2" mỗi năm` → **NOT RUN (budget)**.

**Loop B (benchmark):**
- `Vietnam fossil fuels share of primary energy 2024 ... Energy Institute` → NEDO (citing EI Statistical Review 2024): 2023 primary energy 117 Mtoe, fossil **~71 %** (coal 47 %, oil 24 %, gas not quoted → with gas ~6 % ≈ 77 %); MOIT/VEPG presentation (Apr 2026): coal + oil ≈ **78 % of TPES over 2021–2024**, RE 18.2 Mtoe; Worldometers 2024: fossil **86.7 %** (different accounting); Climate Analytics (IEA 2019): coal 49 % + oil 26 % + gas 9 % = 84 % of energy supply; Enerdata: coal 51 % of total energy. (L2/L4, search extract)
- `Global Carbon Budget 2024 Vietnam fossil CO2` → GCB 2024 global only in results (10.1 GtC fossil 2023); Vietnam number via OWID above. Climate Change Tracker: total GHG ≈ 595 MtCO2e (year unstated); Climate Analytics: 344 MtCO2e GHG in 2022, energy = 63 % of emissions. (L3/L5, search extract)
- `IEA Vietnam CO2 emissions 2023` → **NOT RUN (budget)**.

**Loop C (adversarial):**
- "1,7 triệu tấn" = 1.7 *billion* t? **No** — Vietnam's fossil CO2 is ~0.37–0.43 Gt; 1.7 Gt would be ~4× too high (that is roughly Russia's total). Rejected.
- Sector reading: 1.7 Mt/yr is the scale of a *single* large coal plant (~1 GW) or of the BEST project's claimed lifetime saving (2 Mt). Nothing in the sentence points to a sector.
- Per-capita reading: 1.73 **t/person** (2010) is the only published "1.7" found; the brochure may have dropped "per person" and changed the unit to million tonnes. Today's per-capita is ~3.7–4.3 t (371–431 Mt ÷ ~100 M people), so even that reading is 15 years stale.
- Fossil share: 75 % is **inside** every independent range (71 % EI-2023 excl. gas → 77 % incl. gas; 78 % MOIT; 84–87 % IEA/Worldometers). Confirmed.
- Queries `ourworldindata Vietnam fossil share 2024` → **NOT RUN (budget)**.

**Best evidence level:** L2 (EI/GCB/IEA-EDGAR via secondary extracts; L4 MOIT presentation).
**New verdict:** Split — 75 % fossil share: **Confirmed** (71–87 % depending on dataset; ~77–78 % on EI/MOIT primary-energy basis). "1,7 triệu tấn CO2/năm": **Contradicted** — actual 2023–2024 fossil CO2 is 371–431 Mt, i.e. the claim is low by a factor of **~220–250×**; likeliest origin is the 2010 per-capita figure 1.73 t.
**Confidence:** 0.95 — four independent datasets agree within ±8 %; no reading of "1.7" fits a national total.
**Change vs prior:** refined — same verdicts; updates the range to 371–431 Mt (2024) across GCB/EI/EDGAR, adds the 2010 per-capita origin hypothesis, and widens the fossil-share corroboration (MOIT 78 %, EI 71–77 %).
**What CCS could send to settle it:** the source and year of the "1,7 triệu tấn" figure; proposed fix: "khoảng 75–78 % năng lượng sơ cấp là hóa thạch, phát thải khoảng 370–430 triệu tấn CO2/năm (2024)".
**Sources:** [OWID Vietnam CO2 profile](https://ourworldindata.org/profile/co2/vietnam) (search extract); [Worldometers Vietnam CO2 (EDGAR)](https://www.worldometers.info/co2-emissions/vietnam-co2-emissions/) (search extract); [YCharts, EI series](https://ycharts.com/indicators/viet_nam_carbon_dioxide_emissions) (search extract); [EI Statistical Review downloads](https://www.energyinst.org/statistical-review/resources-and-data-downloads); [NEDO citing EI 2024](https://www.nedo.go.jp/content/800053984.pdf) (search extract); [MOIT/VEPG Apr-2026](https://vepg.vn/wp-content/uploads/2026/04/4.-EN_VNL_DCQHNL-MOIT-VEPG-15.04.2026.pdf) (search extract); [Climate Analytics 1.5 °C pathways VN](https://1p5ndc-pathways.climateanalytics.org/countries/viet-nam/current-situation) (search extract); [OECD Economic Survey VN 2025](https://www.oecd.org/en/publications/oecd-economic-surveys-viet-nam-2025_fb37254b-en/full-report/unlocking-low-carbon-economic-growth_d1fdfa53.html) (search extract); [VJOL per-capita paper](https://vjol.info.vn/JSTD/article/view/19604) (search extract); [Climate Action Tracker VN assumptions](https://climateactiontracker.org/countries/vietnam/assumptions/) (search extract).

---

### F2 — "160 Mt residues; 65 Mt agri/forest residues burned or discarded; 24 Mtoe ≈ USD 28 bn (2022)"
**Quoted (VN):** "Tổng lượng phế phụ phẩm Việt Nam là 160 triệu tấn, trong đó khoảng 65 triệu tấn phụ phẩm nông, lâm nghiệp đang bị đốt, thải bỏ, tiềm năng kinh tế là 24 triệu TOE (tương đương với 28 tỷ USD) (2022)" — Overview p.2.
**Prior verdict:** Needs a source (published crop residues 79–98 Mt).

**Loop A (direct):**
- `"160 triệu tấn" phụ phẩm nông nghiệp` → Dân Việt (28-09-2022), VnEconomy, Báo Đầu tư, Đại Đoàn Kết: "gần 160 triệu tấn" is the press rounding of the MARD figure **156–159 Mt/yr**; TS Tống Xuân Chinh (Cục Chăn nuôi): 2020 total **156.8 Mt** = crop 88.9 Mt + livestock waste 61.4 Mt (+ forestry 5.5 Mt + fisheries ~1 Mt). Utilisation quoted at 10–35 % (most) or 40–50 % (Đại Đoàn Kết). (L4 via press, search extract)
- `"156,8 triệu tấn" phụ phẩm ... 88,9 ... 61,4` → confirms the breakdown and its origin: MARD workshop 10-09-2021, "ước tính lý thuyết" for 2020; rice straw 42.8 Mt, maize stover 10 Mt; collection rate crop 52.2 %, livestock 75.1 %. MAE reply to National Assembly (Jul 2025): ~156 Mt/yr, burning causes GHG/pollution. (L4, search extract)
- `"65 triệu tấn" phụ phẩm nông lâm nghiệp đốt bỏ` → **no source gives 65 Mt burned/discarded.** Related: ~90 Mt crop residues (VJOL), 61.43 Mt from current cropped area (VnBusiness), ~43 Mt rice straw "mostly burned or left to rot" (Nhà Đầu tư). (L4/L5, search extract)
- `"24 triệu TOE" sinh khối Việt Nam` → **not found.** Other TOE figures: wood fuel 75–80 Mt/yr ≈ 26–28 Mtoe (one source); "200 triệu tấn dầu quy đổi" total biomass potential (NTT journal — implausibly high); "99 triệu tấn/năm" biomass potential (another). (L3/L5, search extract)
- `"28 tỷ USD" phụ phẩm nông nghiệp sinh khối` → **not found.** MARD/Báo Đầu tư headline: by-products "có thể mang lại giá trị **4–5 tỷ USD/năm**"; VCCI: "nguồn lợi tỷ USD" unspecified. (L4/L5, search extract)
- `"160 triệu tấn" "65 triệu tấn" ... Oxfam` (to test whether the sentence is copied from the MOIT/Oxfam BEST article) → **NOT RUN (budget)**.

**Loop B (benchmark):**
- `Vietnam agricultural residues energy potential Mtoe ... study` → Beňová et al. 2021 (peer-reviewed): rice straw ~97 Mt/yr → >380 TWh; husk 9 Mt → 35 TWh; bagasse 5 Mt + cane trash 3.5 Mt → 27 TWh; rice + sugarcane ≈ **443 TWh ≈ 38 Mtoe** (theoretical, gross). Other: rice straw 54 Mt/yr (economic-feasibility paper); Scientific Reports: 2,565 MW power potential from straw. (L3, search extract)
- GIZ/IAE residue deck (gizenergy.org.vn, 2022) surfaced in results but could not be opened (blocked). Queries `tiềm năng năng lượng sinh khối "triệu TOE" 2022` and `Vietnam bioenergy potential ... GIZ IRENA 2023 2024` → **NOT RUN (budget)**.
- L1 cross-check: 65 Mt dry residue × 14–16 GJ/t = 910–1,040 PJ = **21.7–24.8 Mtoe** → "24 triệu TOE" is exactly the energy content of 65 Mt at ~15.5 GJ/t. And USD 28 bn ÷ 24 Mtoe = USD 1,167/toe ≈ LPG-equivalent pricing (USD ~900–1,200/toe in 2022), far above crude (USD 733/toe at 100 USD/bbl) or coal (~USD 300–450/toe in 2022).

**Loop C (adversarial):**
- The 160 Mt is **confirmed as a rounding of MARD's 156.8 Mt** — but 61.4 Mt of it is livestock manure, which is not gasifier feedstock; the brochure's wording ("phế phụ phẩm") is defensible, but "phụ phẩm nông, lâm nghiệp" burnable biomass is ~94 Mt (88.9 crop + 5.5 forestry).
- 65 Mt ≈ 69 % of 94 Mt → implies ~31 % utilisation, consistent with the "10–35 %" press range and with MARD's 52 % *collection* rate for crop residues if collected ≠ utilised. Internally coherent, **but no document states 65 Mt**.
- 24 Mtoe is arithmetically the energy content of 65 Mt residue; 28 bn USD values that energy at LPG-replacement prices. Both are derivations, not published statistics, and the USD figure is **~6× MARD's own 4–5 bn USD/yr value estimate** (a different concept: realisable market value vs fuel-replacement value).
- Date "(2022)" fits the Dân Việt/MARD press cycle of Sept 2022 (figures are 2020 data).

**Best evidence level:** L4 (MARD/MAE figures via press and a ministry reply to the National Assembly); L3 for the energy-potential benchmark; L1 for the internal arithmetic.
**New verdict:** Split — 160 Mt total: **Confirmed** (MARD 156.8 Mt, 2020 data, incl. 61 Mt manure). 65 Mt burned/discarded: **Unverifiable** (coherent derivation, no source). 24 Mtoe: **Plausible** (equals 65 Mt × 15.5 GJ/t; in range of peer-reviewed 38 Mtoe gross for rice + sugarcane alone). USD 28 bn: **Overstated / unsourced** (~6× MARD's 4–5 bn USD/yr; only reproducible by pricing at LPG equivalence).
**Confidence:** 0.65 — the headline total is solid; the three derived numbers hang together arithmetically but none has a citable origin, and the dollar figure conflicts with the ministry's own valuation.
**Change vs prior:** upgraded for 160 Mt (source found: MARD 156.8 Mt); refined for the rest (prior "79–98 Mt crop residues" matches the 88.9 Mt crop component).
**What CCS could send to settle it:** the document behind "65 triệu tấn", "24 triệu TOE" and "28 tỷ USD" (title, author, year, page); otherwise re-word to "khoảng 157 triệu tấn phụ phẩm (2020, Bộ NN&PTNT), trong đó ~89 triệu tấn phụ phẩm trồng trọt, tỷ lệ thu gom ~52 %".
**Sources:** [Dân Việt 28-09-2022](https://danviet.vn/print-2022092816262864.htm) (search extract); [VnEconomy "cả trăm triệu tấn"](https://vneconomy.vn/bo-phi-ca-tram-trieu-tan-phu-pham-nong-nghiep-khong-khac-gi-nem-di-hang-ty-usd.htm) (search extract); [Báo Đầu tư 4–5 tỷ USD](https://baodautu.vn/phu-pham-nong-nghiep-viet-nam-co-the-mang-lai-gia-tri-4-5-ty-usdnam-d151278.html) (search extract); [MAE reply to NA deputy, Jul 2025](https://media.mae.gov.vn/Document/f8cdce41-4622-81a8-91d9-5de66d7ee34e//2025/7/11//4317-bnnmt-pc__Tra%20loi%20DBQH%20Tran%20Thi%20Thanh%20Huong%20_signed_4985e1e951.pdf) (search extract); [Nông nghiệp Môi trường (EN) 156 Mt](https://van.nongnghiepmoitruong.vn/turning-156-million-tons-of-agricultural-by-products-into-gold-d302305.html) (search extract); [SGGP "mỏ vàng bị lãng phí"](https://www.sggp.org.vn/phu-pham-trong-nong-nghiep-mo-vang-bi-lang-phi-post615803.html) (search extract); [Beňová 2021, AGRIS record](https://agris.fao.org/search/en/records/67598addc7a957febdfb960a) (search extract); [PMC rice-straw power potential](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7804265/) (search extract); [GIZ/IAE residue deck 2022](https://gizenergy.org.vn/wp-content/uploads/2022%20Document/BEM/2agricultural-residuetrinhieamardvn.pdf) (not opened — blocked); [NTT journal 200 Mtoe](https://jst.ntt.edu.vn/index.php/jst/article/download/811/691/2896) (search extract).

---

### F3 — "WHO: cooking smoke kills 2 million people a year"
**Quoted (VN):** "ô nhiễm khói bếp là nguyên nhân khiến 2 triệu người chết mỗi năm" (WHO) — Household flyer; Service-stove flyer.
**Prior verdict:** Outdated (WHO: 3.2 M for 2020, 2.9 M for 2021).

**Loop A (direct):**
- `WHO household air pollution fact sheet deaths per year 2021 2024` → current WHO fact sheet "Household air pollution and health": **"an estimated 2.9 million deaths per year in 2021, including over 309 000 deaths of children under the age of 5"**; IHD 32 %, stroke 23 %, LRI 21 %, COPD 19 %; combined ambient + household 6.7 M. Earlier snapshot of the same fact sheet: **3.2 million (2020)**, 237,000 children. (L2, search extract)
- `WHO "2 million" deaths household air pollution ... fact sheet 2011` → no copy of a 2 M version surfaced; 2014 version (2012 data): **4.3 million**; 2016 data: **3.8 million**. (L2, search extract)
- `WHO "nearly 2 million people" die indoor air pollution household solid fuel fact sheet` → **null** for the exact phrase; results show the 4.3 M (2014), ~4 M, 2.9 M versions only. Note from memory, **unverified**: WHO Fact Sheet No. 292 (2011) read "Nearly 2 million people a year die prematurely from illness attributable to indoor air pollution from household solid fuel use" (2004 GBD basis). Query `WHO fact sheet 292 2011 ... "nearly 2 million"` → **NOT RUN (budget)**.

**Loop B (benchmark):**
- `Vietnam household air pollution deaths State of Global Air 2024 GBD 2021` → SoGA 2024 (HEI/IHME, 18-06-2024): 8.1 M air-pollution deaths globally in 2021, **38 % from household air pollution (≈ 3.1 M)**, 58 % ambient PM2.5, 6 % ozone. **No Vietnam household-only number** in any result. (L2/L5, search extract)
- `IHME GBD 2021 Vietnam household air pollution solid fuels deaths` → IHME ASEAN Viet Nam profile (2025): air pollution is the **3rd-ranked risk factor** in Vietnam (2021), no household split. (L3/L5, search extract)
- `Vietnam household air pollution deaths 2019 GBD ...` → **NOT RUN (budget)**.

**Loop C (adversarial):**
- Could 2 M be right under a narrower reading? WHO's **child** figure is 0.3 M; the **LRI** share of 2.9 M is 0.6 M; the **COPD + LRI** sum is ~1.2 M. No WHO sub-total equals 2 M.
- Could it be deliberately conservative ("ít nhất 2 triệu")? The flyer says "2 triệu", not "hơn 2 triệu"; the current WHO number is 2.9 M, so "gần 3 triệu" would be both accurate and stronger for CCS.
- Historical reading: the figure matches WHO's 2004-based estimate published 2011 (unverified here), i.e. ~15 years out of date and superseded four times (4.3 M → 3.8 M → 3.2 M → 2.9 M as GBD methods changed).

**Best evidence level:** L2 (WHO fact sheet; SoGA 2024).
**New verdict:** Contradicted (outdated) — understates the current WHO figure (2.9 M, 2021) by ~1.45×.
**Confidence:** 0.90 — WHO's current figure is unambiguous; the only uncertainty is the exact provenance of the "2 million" (pre-2012 WHO sheet, not opened).
**Change vs prior:** none (confirmed) — adds the SoGA 2024 38 % ≈ 3.1 M corroboration and the fact that no Vietnam household-only figure is public.
**What CCS could send to settle it:** nothing needed; replace with "WHO ước tính 2,9 triệu ca tử vong mỗi năm (2021) do ô nhiễm không khí trong nhà từ đun nấu".
**Sources:** [WHO fact sheet HAP](https://www.who.int/news-room/fact-sheets/detail/household-air-pollution-and-health) (search extract); [WHO fs292 archive](https://www.who.int/mediacentre/factsheets/fs292/en/) (search extract); [WASHplus copy of 2014 WHO sheet (4.3 M)](https://washplusblog.fhi360.org/iaqupdates/2014/03/who-fact-sheet-household-air-pollution-and-health/index.html) (search extract); [SoGA 2024 report](https://stateofglobalair.org/resources/report/state-global-air-report-2024) (search extract); [SoGA 2024 webinar slides](https://stateofglobalair.org/sites/default/files/documents/2024-07/soga-webinar2024-slides.pdf) (search extract); [IHME ASEAN Viet Nam profile 2025](https://healthdata-digex.healthdata.org/sites/default/files/2025-06/IHME_ASEAN_template_Viet%20Nam_final_1.pdf) (search extract); [UNICEF VN 3.2 M (2020)](https://www.unicef.org/vietnam/stories/viet-nams-heavy-air-pollution-needs-stronger-action) (search extract).

---

### F4 — "In Vietnam ~60,000 deaths a year are due to air pollution"
**Quoted (VN):** "Tại Việt Nam, khoảng 60.000 ca tử vong hàng năm là do ô nhiễm không khí" — Household flyer.
**Prior verdict:** OK as worded (WHO, all air pollution).

**Loop A (direct):**
- `WHO Việt Nam 60.000 ca tử vong ô nhiễm không khí mỗi năm` → WHO Viet Nam news release **02-05-2018**: "Hơn 60.000 người tử vong năm **2016** do bệnh tim, đột quỵ, ung thư phổi, bệnh phổi tắc nghẽn mãn tính và viêm phổi có liên quan đến ô nhiễm không khí" — covers **ambient + household** together. SGGP and other press repeat 60,000 without the year. (L2, search extract)
- `State of Global Air 2024 Vietnam deaths` → WHO Viet Nam air-pollution topic page now: **"at least 70 000(*) deaths each year are air pollution-related — (*) State of Global Air 2024"**; UN joint op-ed (WHO/UNDP/UNICEF, 5-06-2024): 70,000 deaths/yr, life expectancy shortened 1.4 years. (L2, search extract)
- `WHO Vietnam 2016 household air pollution deaths GHO breakdown` and `"ô nhiễm không khí trong nhà" Việt Nam tử vong WHO` → **NOT RUN (budget)**.

**Loop B (benchmark):**
- `State of Global Air 2024 Vietnam country profile ... 2021 ambient household` → ADB RKSI slide deck (Mar 2025), citing SoGA 2024: Vietnam ranked 10th, **99,700 deaths (2021)**. Discrepancy with WHO's "at least 70,000" (both cite SoGA 2024) — possibly total vs PM2.5-only, or different rounding; unresolved. (L5 citing L2, search extract)
- `State of Global Air 2024 Vietnam "99,700"` → **NOT RUN (budget)**.
- Vietnam **household-only** figure: not given by WHO VN, UNDP, UNICEF, IHME ASEAN profile, or any press item found. The 60,000/70,000 numbers are **all-source** air pollution.

**Loop C (adversarial):**
- Is 60,000 wrong? No — it is WHO's own 2016 estimate. But it is (a) nine years old, (b) superseded by WHO VN's current "ít nhất 70.000", and (c) possibly ~100,000 on the SoGA 2024 basis.
- Risky juxtaposition: the flyer places this sentence directly after the household-smoke claim (F3), inviting readers to attribute 60,000 deaths to cooking smoke. No source supports a household-only Vietnam figure of that size; globally household is ~38–48 % of air-pollution deaths, so a Vietnam household share would be on the order of 20,000–35,000 — **not** published anywhere found.

**Best evidence level:** L2 (WHO Viet Nam 2018 release; WHO VN topic page citing SoGA 2024).
**New verdict:** Confirmed as worded (WHO figure, all air pollution) — but dated; current WHO VN wording is "ít nhất 70.000".
**Confidence:** 0.85 — the 60,000 is traceable to WHO (2016 data); the 0.15 reflects the 70,000 vs 99,700 discrepancy between two readings of SoGA 2024 that could not be resolved without opening the SoGA country data.
**Change vs prior:** refined — same verdict; adds year (2016), the current WHO VN figure (≥70,000, SoGA 2024), the ADB-quoted 99,700 (2021), and the explicit finding that no household-only Vietnam figure exists in the public record.
**What CCS could send to settle it:** nothing needed; update to "Theo WHO, ít nhất 70.000 ca tử vong mỗi năm tại Việt Nam liên quan đến ô nhiễm không khí (State of Global Air 2024)" and keep it visually separate from the cooking-smoke sentence.
**Sources:** [WHO VN 02-05-2018 release (VI)](https://www.who.int/vietnam/vi/news/detail/02-05-2018-more-than-60-000-deaths-in-viet-nam-each-year-linked-to-air-pollution) (search extract); [WHO VN air-pollution topic page](https://www.who.int/vietnam/health-topics/air-pollution) (search extract); [UN joint commentary 5-06-2024](https://www.who.int/vietnam/news/commentaries/detail/tackle-sources-of-air-pollution-to-protect-and-promote-health--development-and-productivity--say-un-agencies-in-viet-nam-to-mark-world-environment-day-(5-june)) (search extract); [UNDP VN blog](https://www.undp.org/vietnam/blog/viet-nams-heavy-air-pollution-needs-stronger-action) (search extract); [ADB RKSI slides Mar-2025 (99,700)](https://rksi.adb.org/wp-content/uploads/2025/03/04-Karma.pdf) (search extract); [SGGP 60,000](https://www.sggp.org.vn/60000-ca-tu-vong-moi-nam-tai-viet-nam-do-o-nhiem-khong-khi-gay-ra-post532091.html) (search extract); [NGO Centre news (60,000, WHO)](https://ngocentre.org.vn/news/vietnam-records-60000-deaths-linked-air-pollutionyear-who) (search extract).

---

## Summary table

| ID | Prior | New | Level | Confidence | Changed? |
|---|---|---|---|---|---|
| E1 | Contradicted (20 t/h ≈ 14.9 MW) | **Contradicted** — 20 t/h = 13–15 MW steam / 16–19 MW fuel (4–6× the 3 MW ceiling); 20 kg/h = 15 kW (20× below 300 kW floor); none of 5 named boiler sites found with a size | L1 | 0.90 | refined |
| E2 | Needs proof | **Unverifiable** — public record holds only BEST *targets* (2,500 MSEs/100/400; 1.4 Mt; 2 MtCO2e), an EU "behind schedule" note, and a MOIT line that no biomass model is widely applied; "1000+" appears nowhere else; World Vision 2025 not found | L5 | 0.55 | refined |
| F1 | 75 % Confirmed; 1.7 Mt Wrong | 75 %: **Confirmed** (71–87 %; ~77–78 % EI/MOIT). 1.7 Mt: **Contradicted** — actual 371–431 Mt (2024), ~220–250× higher; likely origin 1.73 t *per capita* (2010) | L2 | 0.95 | refined |
| F2 | Needs a source | 160 Mt: **Confirmed** (MARD 156.8 Mt, 2020; incl. 61 Mt manure). 65 Mt: **Unverifiable**. 24 Mtoe: **Plausible** (= 65 Mt × 15.5 GJ/t). USD 28 bn: **Overstated/unsourced** (~6× MARD's 4–5 bn USD/yr) | L4 | 0.65 | upgraded (160 Mt) / refined |
| F3 | Outdated | **Contradicted (outdated)** — WHO now 2.9 M (2021); 3.2 M (2020); SoGA 2024 ≈ 3.1 M; "2 M" is a pre-2012 WHO figure | L2 | 0.90 | none |
| F4 | OK as worded | **Confirmed as worded, dated** — WHO 60,000 is 2016 data; WHO VN now "≥ 70,000" (SoGA 2024); ADB quotes SoGA 2024 as 99,700 (2021); no household-only VN figure exists | L2 | 0.85 | refined |

## Gaps for loop 2
Blocked this pass by (a) proxy 403 on all external hosts and (b) the shared 200-search budget. In priority order:

1. **Open the primary pages** that were only seen as search extracts: WHO HAP fact sheet (confirm "2.9 million, 2021" and the sheet's revision date); WHO VN 2018 release and current topic page; SoGA 2024 Vietnam country data (resolve 70,000 vs 99,700; get the household-only Vietnam number — IHME GBD 2021 "household air pollution from solid fuels", Vietnam, deaths); OWID/GCB 2024 Vietnam CO2; EI Statistical Review 2025 data workbook (Vietnam "CO2 from energy" 2023–2024 and fossil share of primary energy); Dân Việt 28-09-2022 and the MAE Jul-2025 National Assembly reply (exact 156.8 Mt wording); GIZ/IAE 2022 residue deck (per-crop tonnages, PJ/Mtoe); BEST impact sheet, SWITCH-Asia project page and the Feb-2025 final-evaluation ToR (any progress numbers in the background section).
2. **E1 — not run:** `"Quang Bình" Hà Giang chè khí hóa sinh khối` (correct district spelling); `site:ccs.org.vn lò hơi`; `site:ccspin.org lò hơi`; `"khí hóa sinh khối" "tấn hơi" 2024 2025`; `"Nồi hơi Việt Nam" khí hóa 2012 công suất`; company-registry lookups for "Tre Xứ Thanh" and "Vipagro" (dangkykinhdoanh.gov.vn).
3. **E2 — not run:** `hội thảo tổng kết dự án BEST 2024`; `BEST mid-term review 2023 VCBG units`; `"Nguyễn Hồng Long" ... chuyển giao`; `"Tầm nhìn Thế giới" Thanh Hóa bếp 2025` / `World Vision Việt Nam Thường Xuân bếp sinh khối`; `congthuong.vn "khí hóa sinh khối" 2024 2025` (locate the "chưa được nhân rộng" article); Oxfam VN "Dinh Hoa" and "Women at the forefront" stories for any unit counts; ask whether the BEST final evaluation (2025) is public.
4. **F1 — not run:** `"1,7 triệu tấn CO2" mỗi năm` (origin hunt); `IEA Vietnam CO2 2023 country profile`; OWID energy profile Vietnam fossil share 2024 (to pin the ~77 % figure to EI 2025).
5. **F2 — not run:** `"160 triệu tấn" "65 triệu tấn" ... Oxfam/MOIT` (test whether Overview p.2 copies the BEST launch article — the MOIT/bavutex repost may carry the 65 Mt / 24 Mtoe / 28 bn text); `"triệu TOE" phụ phẩm 2022`; `Vietnam bioenergy potential GIZ/IRENA 2023 2024`; `phụ phẩm trồng trọt tỷ lệ sử dụng 30 %`.
6. **F3 — not run:** `WHO fact sheet 292 2011 "nearly 2 million"` (verify the provenance stated above from memory; try web.archive.org copy of who.int/mediacentre/factsheets/fs292, 2011–2013); `Vietnam household air pollution deaths GBD 2019/2021`.
7. **F4 — not run:** `SoGA 2024 Vietnam "99,700"`; `WHO GHO Vietnam 2016 household vs ambient deaths`; Vietnamese press on "ô nhiễm không khí trong nhà" deaths.
