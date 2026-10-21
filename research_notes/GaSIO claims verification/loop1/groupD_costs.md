# Group D — Fuel-cost savings and price (D1–D5) — Loop 1 notes

**Agent run:** 2026-10-21. **Method:** PROTOCOL.md three-loop rule. 26 WebSearch calls were run (logged below per claim); the shared per-turn search budget was then exhausted, and 7 further planned queries could not be run (listed in "Gaps for loop 2"). WebFetch resolved only one host (the Oxfam S3 bucket): every other fetch failed with DNS/proxy errors (hosts listed at the end), so all other citations are **(search extract)** and graded accordingly. One primary document was obtained and text-extracted locally: the Oxfam/CCS VCBG brochure (2021), saved at `/tmp/claude-0/-home-user-Kevin-s-fun-things/206939fd-f22b-5d72-8316-eca6446ec6c9/scratchpad/dl_vcbg/vcbg_brochure.pdf`.

**Exchange rate used:** ≈26,000 VND/USD (2025–26 range 25,500–26,300; approximate).

---

## 0. Price and efficiency inputs gathered (dated)

### 0.1 Baseline fuel prices, Vietnam, 2024–2026

| Fuel | Price | Date / basis | Source (level) |
|---|---|---|---|
| LPG, Petrolimex Hà Nội, 12 kg household cylinder | 409,600 VND (34,133 VND/kg); world CP 485 USD/t | Oct 2025 | thoibaotaichinhvietnam.vn (L5, search extract) |
| LPG, Petrolimex Hà Nội, 12 kg | 411,500 VND | Dec 2025 | thoibaotaichinhvietnam.vn (L5, search extract) |
| LPG, Saigon Petro 12 kg | 452,500 VND | early Mar 2026 | thoibaotaichinhvietnam.vn (L5, search extract) |
| LPG, Petrolimex 12 kg Hà Nội / TP HCM | 598,104 / 592,000 VND (≈49,800 VND/kg) | Jun 2026 | thoibaotaichinhvietnam.vn (L5, search extract) |
| LPG per kg quoted by boiler vendor | 16,000–20,000 VND/kg (bulk/industrial, undated, low) | undated | hex-boilers.com (L6, search extract) |
| Electricity, average retail | 2,204.07 VND/kWh ex-VAT (+4.8%), Decision 599/QĐ-EVN & 1279/QĐ-BCT | from 10 May 2025 | vneconomy, baophapluat, thoibaotaichinhvietnam (L4 decree via L5 press, search extract) |
| Electricity, household tiers 1–6 | 1,984 / 2,050 / 2,380 / 2,998 / 3,350 / 3,460 VND/kWh ex-VAT | from 10 May 2025 | chogia.vn (L6, search extract) — arithmetically consistent with the Oct-2024 tiers ×1.048, so accepted |
| Electricity, production <6 kV normal hours | ≈1,896 VND/kWh ex-VAT (derived: 1,809 Oct-2024 × 1.048) — **not fetched, needs loop-2 check** | May 2025 | derivation (L4 schedule from memory) |
| Electricity, business <6 kV normal hours | ≈3,008 VND/kWh ex-VAT (derived: 2,870 × 1.048) — **needs check** | May 2025 | derivation |
| Coal, domestic than cám 5a | 1.815–1.85 M VND/t incl VAT + delivery | 2025 | thanda.net (L6 vendor, search extract) |
| Coal, domestic than cám 6a | 1.48–1.51 M VND/t incl VAT + delivery | 2025 | thanda.net (L6 vendor, search extract) |
| Coal, "than cám 5" retail | ≈2,100 VND/kg | early 2025 | kinhdoanhthannhapkhau.com (L6, search extract) |
| Coal, Indonesian GAR 3400–4200 | 1.1–1.6 M VND/t ex-VAT ex-transport | Feb–Apr 2026 | vietanenergy.com.vn, thanvietan.com (L6, search extract) |
| Coal, Indonesian GAR 5000 / 5800 | 2.2–2.5 / 2.6–2.85 M VND/t | Apr 2026 | vietanenergy.com.vn (L6, search extract) |
| Coal, TKV official 2025 price list for cám 4b/5a/6a | **not found** — only 2016 TKV notices surfaced (cám 1: 2.6 M; cám 7A: 0.785 M VND/t) | — | moit.gov.vn, vinanet.vn (L4, search extract) |
| Firewood (gỗ củi), Thái Nguyên farm-gate | 800–900 VND/kg; acacia 730–750k VND/m³ standing | Feb 2024 | baothainguyen.vn (L5, search extract) |
| Firewood, boiler vendor | 800–1,200 VND/kg | undated | hex-boilers.com (L6, search extract) |
| Firewood, Techno Wood price list (keo) | 2.0 M VND/khối (branch) – 2.75 M VND/khối (dried split) | 2025 | technowood.vn (L6 seller quote, search extract) |
| Firewood, northern dry split, delivered | 1.5–3.0 M VND/m³ | undated | thancuihoangphuong.com (L6, search extract) |
| Acacia / eucalyptus roundwood for chips | >1.2 / >1.1 M VND/t | late 2025–early 2026 | ai-hay.vn (L6, low reliability) |
| Rice husk, raw | 400–500 VND/kg (SGT, undated); 700–800 VND/kg (Dân trí, older); >1,000 VND/kg some places (older) | undated/older | thesaigontimes.vn, dantri.com.vn (L5, search extract) — **no 2024–26 raw-husk price found** |
| Rice-husk briquettes (củi trấu) | 1,300–1,500 VND/kg wholesale | older | dantri, nhipcaudautu (L5, search extract) |
| Rice-husk pellets | 1,800–2,500 VND/kg | Mar 2025 | kinhdoanhthannhapkhau.com (L6, search extract) |
| Wood pellets, domestic boiler grade | 2.5–3.8 M VND/t (May 2025); 3,090 VND/kg (15 Oct 2026); 3,000 VND/kg min 10 t | 2025–2026 | kinhdoanhthannhapkhau.com, nhienlieulohoi.vn, chatdotlohoi.vn (L6, search extract) |
| Wood pellets, export average | 147.8 USD/t H1-2026 (+2.3% vs 2025) | 2026 | VIFOREST via mekongasean.vn (L5, search extract) |
| Sawdust (mùn cưa) loose | **not found** (two searches null; only briquette LHV 4,300–4,800 kcal/kg, price "liên hệ") | — | trangvangvietnam.com (L6) |
| Corn cob (lõi ngô) | **not found** (search null) | — | — |

### 0.2 Heating values and appliance efficiencies used
LPG 46 MJ/kg; electricity 3.6 MJ/kWh; coal 17.6–24 MJ/kg by grade (GAR 4200 = 17.6; cám 6a ≈ 21; cám 5a ≈ 24); air-dry firewood/chips 15 MJ/kg; rice husk 13.5 MJ/kg; wood pellets 18 MJ/kg (vendor LHV 4,300–4,800 kcal/kg); husk pellets 15 MJ/kg.
Efficiencies: LPG household stove 55–60%; LPG direct flame on a tea drum 40–60%; resistive electric 85–95%; heat pump COP 3–4; small coal boiler 60–75%; traditional wood stove 15–30% (VNUF 2024 measured a traditional stove at 16.8% — vjol.info.vn, L3 search extract); improved wood furnace 35%; GaSIO 50% (ISO 19867-3 Tier-5 floor, L2) to 73% (CCS's own claim, L6). These efficiency benchmarks are standard literature values and were **not re-fetched this loop** (search budget) — flagged for loop 2.

### 0.3 Computed cost of useful heat (VND per useful MJ), 2025–26 prices
Script: `/tmp/claude-0/-home-user-Kevin-s-fun-things/206939fd-f22b-5d72-8316-eca6446ec6c9/scratchpad/scripts/costs.py` (L1 arithmetic on the inputs above).

| Baseline | VND/MJ useful |
|---|---|
| LPG household stove 55–60% (34,133–49,842 VND/kg) | 1,237–1,970 |
| LPG industrial 45 kg (~31,000–45,000 VND/kg), burner 55–60% | 1,123–1,779 |
| Electricity household tiers 3–6 incl VAT, resistive 85–95% | 752–1,221 |
| Electricity production tariff (~1,896 ex-VAT), resistive | 599–669 |
| Electricity business tariff (~3,008 ex-VAT), resistive | 950–1,062 |
| Electricity production tariff, heat pump COP 3–4 | 142–190 |
| Coal cám 6a, boiler 60–75% | 94–120 |
| Coal cám 5a, boiler 60–75% | 101–128 |
| Coal Indo GAR 4200, boiler 60–75% | 83–152 |
| Coal Indo GAR 5000, boiler 60–75% | 140–199 |
| Firewood 800–1,500 VND/kg, traditional stove 15–30% | 178–667 |
| Firewood, improved furnace 35% | 152–286 |

| GaSIO fuel (η 50–73%) | VND/MJ useful |
|---|---|
| Rice husk 500–1,000 VND/kg | 51–148 |
| Wood chips/branches 1,000–1,500 VND/kg | 91–200 |
| Firewood 800–1,500 VND/kg | 73–200 |
| Husk pellets 1,800–2,500 VND/kg | 164–333 |
| Wood pellets 2,500–3,800 VND/kg | 190–422 |

Resulting saving ranges (worst-case to best-case combination):

| Comparison | GaSIO on chips | GaSIO on husk | GaSIO on wood pellets | CCS claims |
|---|---|---|---|---|
| vs LPG household stove | +84% to +95% | +88% to +97% | +66% to +90% | 77 / 80 / 85 / 80–90% |
| vs LPG industrial burner / tea drum | +82% to +96% | +87% to +98% | +62% to +92% | 77%, 85% (tea) |
| vs electricity, household resistive | +73% to +93% | +80% to +96% | +44% to +84% | 90% ("10 lần"), 50% |
| vs electricity, production tariff resistive | +67% to +86% | +75% to +92% | +29% to +72% | 50% |
| vs electricity, heat-pump dryer COP 3–4 | −41% to +52% | −4% to +73% | −197% to 0% | 50% |
| vs coal cám 6a / 5a boiler | −113% to +29% | −58% to +61% | −349% to −48% | 40 / 50 / 54% |
| vs coal Indo GAR 4200 | −140% to +40% | −78% to +67% | −407% to −26% | 40 / 50 / 54% |
| vs coal Indo GAR 5000 | −42% to +54% | −6% to +75% | −201% to +5% | 40 / 50 / 54% |
| vs firewood traditional stove 15–30% (same wood price) | efficiency-only: +40% to +79% | — | — | 50%, 30–50%, 20% |
| vs firewood improved furnace 35% | efficiency-only: +30% to +52% | — | — | 20% (tea) |

---

### D1 — Saving vs coal (40% / 50% / 54%)
**Quoted (VN):** "Tiết kiệm đến 40% chi phí nhiên liệu so với sử dụng than đá" — Overview, p.2; "Giảm 50% so với sử dụng than" — Overview, p.6; "Tiết kiệm 54% chi phí so với dùng than" — Overview, p.14
**Prior verdict:** Contradicted
**Loop A (direct):** (1) `SWITCH-Asia BEST project Vietnam biomass gasification cost-benefit analysis report` → no CBA report found; EEAS/Oxfam project pages only (targets: 1.4 Mt biomass, 2 Mt CO2e; a "standard cost-benefit calculation" study is listed as planned on the Oxfam project page) — L5 (search extract). (2) `CCS GaSIO bếp khí hóa tiết kiệm chi phí nhiên liệu so với gas than củi ccs.org.vn` → no ccs.org.vn page indexed; SWITCH-Asia VCBG user manual (3__best_vcbg_user_manual_vnm.pdf) gives tea-firing savings "10–30% so với củi, 70% so với điện, 80% so với gas" — no coal figure — L5/L6 (search extract; fetch blocked 403). (3) Oxfam/CCS VCBG brochure PDF (fetched, pdftotext, InDesign file dated 7 Apr 2021, 2 pp): "Tiết kiệm tới 50% chi phí so với đốt bằng than đá và 80% chi phí so với đốt bằng gas hoặc dầu" — L6 (CCS/Oxfam own statement, qualified "tới" = up to). (4) `Oxfam Vietnam BEST project final evaluation report ...` → final evaluation not found; only mid-term-review ToR; Tran Nam tea facility "saved 10–15 million VND/month in gas"; story "VCBG stoves cut fuel expenses 20–30% vs traditional wood stoves" — L5 (search extract). No coal-specific project measurement found.
**Loop B (benchmark):** (1) `giá than cám 4b 5a 6a 2025 đồng/tấn nồi hơi TKV` → no 2025 TKV list; old TKV notices only — null for 2025 (L4 search extract). (2) `"giá than" đốt lò hơi 2025 "than cám 5"...` → Indo coal 1.1–2.85 M VND/t by GAR (Feb–Apr 2026); than cám 5 ≈2,100 VND/kg (early 2025) — L6 vendors (search extract). (3) `TKV giá bán than cám 2025 "than cám 5a"...` → thanda.net 2025: cám 5a 1.815–1.85 M, cám 6a 1.48–1.51 M VND/t incl VAT+delivery — L6 (search extract). (4) Biomass prices: chips/roundwood 1.1–1.5 M VND/t; pellets 2.5–3.8 M VND/t (2025–26); husk pellets 1.8–2.5 M VND/t (Mar 2025); raw husk no current price (section 0.1). Computation (L1): at these prices GaSIO on wood chips saves −113% to +40% vs coal boilers; only cheap residue (husk ≤1,000 VND/kg) reaches 50–75%; pellets are always dearer than coal per useful MJ.
**Loop C (adversarial):** (1) Price-snapshot hypothesis: the C6 industrial tea flyer implies 1,100 t coal ↔ 1,500 t biomass; saving = 1 − 1,500·P_bio/(1,100·P_coal). At 2022 spike prices (Indo coal 2.5–3.5 M VND/t) and biomass 1.0–1.2 M VND/t the saving is 35–61%, so 40–54% is reproducible if CCS's figures date from 2022 or assume waste residue at ≤0.8 M VND/t — not searchable this loop (budget), logged as hypothesis. (2) "Tới 50%" in the 2021 Oxfam brochure vs unqualified "Giảm 50%" on Overview p.6: the Overview dropped the "up to". (3) Efficiency reading: if a gasifier burner reaches 73% vs a 60% coal boiler, the efficiency term alone adds ~18% saving — included in the ranges above. (4) Query `giá mùn cưa / lõi ngô / vỏ cà phê` → null; cannot test the "free residue" reading with 2025 prices.
**Best evidence level:** L1 arithmetic on L5/L6 price inputs (no L3/L4 coal-vs-biomass cost study found)
**New verdict:** Contradicted (internal 40/50/54 for the same comparison) and Overstated at 2025–26 prices: with domestic cám 5a/6a or Indo GAR 4200 coal at 1.4–1.85 M VND/t and biomass chips at 1.0–1.5 M VND/t, the computed saving is −113% to +40%; 50–54% needs residue ≤0.8 M VND/t or coal ≥2.5 M VND/t.
**Confidence:** 0.6 — price inputs are vendor quotes (L6) and the TKV official list was not found; the direction (coal is cheap per MJ in Vietnam, pellets are not) is robust.
**Change vs prior:** refined — kept Contradicted, added that even the lowest figure (40%) is only supportable under cheap-residue or 2022-price assumptions, and that the 2021 Oxfam brochure said "tới 50%" (up to).
**What CCS could send to settle it:** the price table (date, VND/t, kcal/kg) behind each percentage; the BEST "standard cost-benefit calculation" study; one metered coal-boiler-to-gasifier conversion with fuel invoices for ≥3 months.
**Sources:** [Oxfam/CCS VCBG brochure PDF (fetched)](https://oi-files-cng-v2-prod.s3.eu-west-2.amazonaws.com/vietnam.oxfam.org/s3fs-public/file_attachments/Brochure%20VCBG%20-%20final.pdf); [SWITCH-Asia VCBG user manual (search extract, fetch 403)](https://www.switch-asia.eu/site/assets/files/4632/3__best_vcbg_user_manual_vnm.pdf); [SWITCH-Asia BEST project page](https://switch-asia.eu/project/biomass-gasification-technology); [Oxfam BEST project page](https://vietnam.oxfam.org/what-we-do-secured-livelihoods-and-resilient-communities/biomass-gasification-technology-sustainable); [thanda.net 2025 cám prices (search extract)](https://thanda.net/gia-than-cam-2a-5ab-6ab-8c/); [vietanenergy Indo coal Apr 2026 (search extract)](https://vietanenergy.com.vn/gia-than-cam-indonesia/); [kinhdoanhthannhapkhau coal retail (search extract)](https://kinhdoanhthannhapkhau.com/gia-than-da-ban-le-hien-nay/); [MOIT: TKV 2016 price notice (search extract)](https://moit.gov.vn/tin-tuc/thi-truong-nuoc-ngoai/tkv-dieu-chinh-gia-ban-cho-8-loai-than-cam.html); [kinhdoanhthannhapkhau pellets May 2025 (search extract)](https://kinhdoanhthannhapkhau.com/bao-gia-vien-nen-go-moi-nhat/); [nhienlieulohoi.vn pellets Oct 2026 (search extract)](https://nhienlieulohoi.vn/san-pham/vien-nen-go/)

---

### D2 — Saving vs LPG/gas (80% / 77% / "15%" / "5–10 lần")
**Quoted (VN):** "80% chi phí so với đốt bằng LPG hoặc dầu" — Overview, p.2; "Tiết kiệm 77% chi phí so với dùng Gas" — Overview, p.14; "chi phí chỉ bằng 15% so với sao chè bằng LPG" — Brochure; "05 - 10 lần so với đun bằng gas" — Household flyer
**Prior verdict:** Contradicted
**Loop A (direct):** (1) `CCS GaSIO ... ccs.org.vn` → SWITCH-Asia BEST VCBG user manual: tea firing saves "80% so với gas" — L5/L6 (search extract). (2) `SWITCH-Asia BEST ... cost-benefit` → Oxfam Vietnam node/1219 summary of project research on green tea: savings "69% compared to gas stoves" per kg finished tea using chipped branches (also 34% vs wood, 19% vs electric; 50 M VND/yr labour) — L5 (search extract; fetch failed). (3) Oxfam/CCS 2021 brochure (fetched): "80% chi phí so với đốt bằng gas hoặc dầu" — L6. (4) `Oxfam ... final evaluation` → Tran Nam cooperative "saved 10–15 million VND/month in gas"; ADB SEADS "about 15 million VND/month in gas and electricity" — L5 self-reported single site (search extract). (5) `ccspin.org OR ccs.org.vn ... Nguyễn Hồng Long` → Genk (Oct 2017): Long says energy cost "giảm khoảng 2/3 so với các loại bếp sử dụng nhiên liệu khí hóa lỏng hay dầu diesel" (≈67%) — L6 (search extract).
**Loop B (benchmark):** (1) `giá gas tháng 10/2025 bình 12kg Petrolimex Saigon Petro` → 409,600 VND/12 kg Hà Nội Oct 2025; 411,500 Dec 2025 — L5 (search extract). (2) `giá gas tháng 10/2026 ...` → 598,104 VND/12 kg Hà Nội, 592,000 TP HCM (Jun 2026); Saigon Petro 452,500 (Mar 2026) — L5 (search extract); Oct 2026 figure not found. (3) `sao chè chi phí nhiên liệu 1 kg chè khô ...` → Việt Phát (vendor): a 45 kg cylinder fires ≈80 kg dry tea (0.56 kg LPG/kg tea) → 19,200–28,000 VND fuel per kg tea at 2025–26 prices; hex-boilers vendor lists củi 800–1,200 VND/kg, gas 16,000–20,000 VND/kg — L6 (search extract). Computation (L1): GaSIO on chips vs LPG household stove +84% to +95%; vs LPG tea drum (equal burner efficiency, fuel-price ratio only) 87–94% with chips at 1,000–1,500 VND/kg, 73–82% with pellets at 3,000 VND/kg. So 77%, 80%, 85% and "5–10 lần" (80–90%) are each inside the computed range; 77–80% corresponds to pellet-grade fuel, 85–90% to chips/branches.
**Loop C (adversarial):** (1) Same-application contradiction: Overview p.14 (77%) and Brochure (85%, "15%") both describe tea firing vs gas; the project's own measured figure is 69% (Oxfam research) and CCS's 2017 figure was ≈67% — the spread 67–85% for the same use is the real inconsistency. (2) LPG price drift reading: the 2026 LPG spike (+46% vs Oct 2025) raises any saving; a 69% result at 2023–24 prices would be ≈75–78% at Jun-2026 prices — this reconciles 69%→77% but not 85–90%. (3) "5–10 lần" is a ratio (80–90% saving); reachable only with household LPG prices and residue ≤1,500 VND/kg at ≥50% stove efficiency. (4) Fuel-type reading: if the GaSIO user buys wood pellets (3,000–3,800 VND/kg) the saving drops to 62–73% — below every brochure figure.
**Best evidence level:** L5 (project's own research summary 69%) + L1 arithmetic on L5 LPG prices
**New verdict:** Contradicted (internal: 67–69% measured/early vs 77–90% in current brochures for the same tea use) — but every individual figure is Plausible as a theoretical range at 2025–26 LPG prices; the "15% of LPG cost" (85% saving) needs chips ≤1,500 VND/kg and is above the project's measured 69%.
**Confidence:** 0.7 — LPG prices are well dated (L5 press); the measured 69% is a search extract of an Oxfam summary whose method is unknown.
**Change vs prior:** refined — kept Contradicted, but downgraded severity: the physics/price arithmetic supports 75–92%, so the problem is inconsistency and the gap to the project's measured 69%, not impossibility.
**What CCS could send to settle it:** the Oxfam/BEST tea-processing fuel study (kg fuel per kg dry tea for LPG vs VCBG, prices and dates); fuel invoices from Tran Nam or another cooperative before/after.
**Sources:** [Oxfam VN node/1219 (search extract)](https://vietnam.oxfam.org/node/1219); [SWITCH-Asia VCBG user manual (search extract)](https://www.switch-asia.eu/site/assets/files/4632/3__best_vcbg_user_manual_vnm.pdf); [Oxfam/CCS 2021 brochure (fetched)](https://oi-files-cng-v2-prod.s3.eu-west-2.amazonaws.com/vietnam.oxfam.org/s3fs-public/file_attachments/Brochure%20VCBG%20-%20final.pdf); [ADB SEADS green technology article](https://seads.adb.org/articles/green-technology-driving-force-agriculture-viet-nam); [Oxfam story Dinh Hoa](https://vietnam.oxfam.org/latest/stories/when-waste-reduces-environmental-pollution-story-dinh-hoa-thai-nguyen); [Genk 2017 CCS interview (search extract)](https://genk.vn/con-nho-startup-viet-che-tao-bep-sach-hieu-suat-cao-nhat-the-gioi-khong-ho-lai-vua-co-them-mot-cai-gi-do-dau-tien-tren-the-gioi-nua-20171019183316136.chn); [Gas price Oct 2025 (search extract)](https://thoibaotaichinhvietnam.vn/gia-gas-ban-le-trong-nuoc-thang-102025-dao-chieu-giam-184151.html); [Gas price Dec 2025 (search extract)](https://thoibaotaichinhvietnam.vn/gia-gas-ban-le-trong-nuoc-thang-12-dao-chieu-tang-187854.html); [Gas price Jun 2026 (search extract)](https://thoibaotaichinhvietnam.vn/gia-gas-ban-le-thang-62026-tiep-tuc-tang-198331.html); [Việt Phát gas tea roaster (search extract)](https://congnghevietphat.com/may-sao-che-bang-gas-vps-01g.html); [hex-boilers fuel comparison (search extract)](https://hex-boilers.com/so-sanh-gia-lo-hoi-dot-cui-va-cac-loai-nhien-lieu-khac.html)

---

### D3 — Saving vs electricity ("10 lần" vs 50%)
**Quoted (VN):** "rẻ hơn 10 lần so với đun bằng điện" — Brochure; "Giảm 50% so với sử dụng điện" — Green-tea flyer and Overview, p.12
**Prior verdict:** Contradicted (rough check ≈3.6x)
**Loop A (direct):** (1) SWITCH-Asia VCBG user manual: "70% so với điện" for tea firing — L5/L6 (search extract). (2) Oxfam node/1219 research summary: "19% compared to electric stoves" per kg finished tea — L5 (search extract). (3) ADB/Oxfam: Tran Nam ~15 M VND/month saved on gas+electricity (unsplit) — L5 (search extract). (4) `ccspin.org ...` and `CCS GaSIO ...` → no CCS page giving an electricity figure found; tietkiemnangluong.com.vn/VNCPC: cooking cost "1.500 đồng cho một bữa ăn gia đình" (no electricity comparison) — L6 (search extract).
**Loop B (benchmark):** (1) `giá điện bán lẻ bậc thang EVN 2025 ...` → average 2,204.07 VND/kWh ex-VAT from 10 May 2025 (Decision 599/QĐ-EVN; 1279/QĐ-BCT); household tiers 1,984–3,460 ex-VAT — L4 decree via L5/L6 (search extract). (2) `evn.com.vn biểu giá ... ngành sản xuất` → production-tariff table not surfaced; derived ≈1,896 VND/kWh (<6 kV, normal hours) from the Oct-2024 schedule ×1.048 — unverified. Computation (L1): household resistive 752–1,221 VND/MJ useful vs GaSIO chips 91–200 → 3.8–13x (73–93% saving); production tariff 599–669 vs chips → 3–7x (67–86%); heat-pump dryer COP 3–4 → GaSIO saves −41% to +52%.
**Loop C (adversarial):** (1) Is 10x reachable? Yes only with CCS's own 73% efficiency and residue ≤1,000 VND/kg against household tiers 4–6; with the ISO Tier-5 floor (50%) the ratio is 3.8–9x. (2) Tea-roasting reading: electric drum roasters put heat directly into the drum (high effective efficiency), which is why the project's own research found only 19% — the 50% on the Green-tea flyer is already above the measured 19%, and 10x (90%) is far above it. (3) Application reading: Overview p.12 (hybrid solar dryer) at 50% vs electric resistive drying is plausible; vs a heat-pump dryer it is not. (4) The search `giá điện mới nhất 2026 ...` to check for a 2026 tariff change was **not run (budget exhausted)**.
**Best evidence level:** L1 arithmetic on L4 tariff (May 2025) + L5 project research summary
**New verdict:** Contradicted (internal: 10x vs 2x vs project-measured 1.2x for tea) — the brochure's "10 lần" is Overstated: central estimate 4–8x for household cooking, 3–7x at production tariff, and 1.2–3x for tea roasting per BEST's own data; "Giảm 50%" is conservative for cooking and optimistic for tea roasting.
**Confidence:** 0.7 — tariff is official and dated; the 19% figure is a search extract; the production tariff was derived not fetched.
**Change vs prior:** refined — the prior "≈3.6x" is confirmed as the low-central case (production tariff, Tier-5 efficiency); 10x is possible only at the extreme (household tier 4–6, 73% efficiency, ≤1,000 VND/kg residue).
**What CCS could send to settle it:** kWh per kg dry tea for the electric roaster baseline, kg biomass per kg tea for VCBG, with tariff tier and fuel price used.
**Sources:** [Decision 599/QĐ-EVN coverage (search extract)](https://vneconomy.vn/tang-gia-ban-le-dien-binh-quan-them-4-8.htm); [baophapluat 2,204 VND/kWh (search extract)](https://baophapluat.vn/gia-dien-ban-le-binh-quan-tang-48-len-hon-2204-dongkwh-tu-ngay-105-post547893.html); [luatvietnam tier impact (search extract)](https://luatvietnam.vn/linh-vuc-khac/tu-ngay-10-5-2025-khach-hang-se-tra-them-bao-nhieu-tien-dien-moi-thang-883-102060-article.html); [chogia.vn tier table (search extract)](https://chogia.vn/gia-dien-sinh-hoat-gia-dien-kinh-doanh/); [lsvn.vn two-part tariff pilot Oct 2025 (search extract)](https://lsvn.vn/thu-nghiem-gia-ban-le-dien-2-thanh-phan-tu-thang-10-2025-a164466.html); [Oxfam VN node/1219 (search extract)](https://vietnam.oxfam.org/node/1219); [SWITCH-Asia VCBG user manual (search extract)](https://www.switch-asia.eu/site/assets/files/4632/3__best_vcbg_user_manual_vnm.pdf); [VNCPC 1,500 VND/meal (search extract)](https://vncpc.org/bep-khi-hoa-sinh-khoi-giai-phap-tiet-kiem-nang-luong/)

---

### D4 — Saving vs firewood (50% / 30–50% / 20%)
**Quoted (VN):** "giá bằng một nửa so với đun củi" — Brochure; "30% - 50% so với đun củi" — Household flyer; "Giảm 20% so với sử dụng củi" — Green-tea flyer
**Prior verdict:** Contradicted (may be product differences)
**Loop A (direct):** (1) SWITCH-Asia VCBG user manual: tea firing "10–30% so với củi" — L5/L6 (search extract). (2) Oxfam node/1219: "34% compared to wood" per kg finished tea — L5 (search extract). (3) Oxfam story (Dinh Hoa): "VCBG stoves cut fuel expenses by 20–30% compared with traditional wood stoves" — L5 (search extract). (4) baothainguyen.vn Dec 2024: Tota chipped-wood furnace in Đại Từ "tiết kiệm tới 30% so với các lò đốt theo phương pháp thông thường" (maker unclear; not confirmed as CCS) — L5 (search extract). (5) tiasang.com.vn: competitor Thế Hệ Xanh natural-draft gasifier claims 50–60% less firewood than a traditional stove — L6 (search extract).
**Loop B (benchmark):** (1) `giá củi đốt 2025 đồng/kg ...` → null (foreign results only). (2) `"giá củi" 2025 "đồng/kg" ...` → Thái Nguyên Feb 2024: 800–900 VND/kg gỗ củi (L5); vendors 800–1,200 VND/kg; 1.5–3.0 M VND/m³ delivered split (L6) — search extracts. (3) `bếp khí hóa sinh khối giá bán 2025 ...` → Vietnam Forestry University 2024 paper (vjol.info.vn 106721): gasifier stove thermal efficiency 21.9% vs traditional 16.8% → same-fuel saving 23% — L3 (search extract; stove identity vs GaSIO unconfirmed). Computation (L1): saving with the same fuel = 1 − η_trad/η_gas: 40–79% for η_trad 15–30% vs η_gas 50–73%; 30–52% vs an improved 35% furnace; 23% per the VNUF measurement.
**Loop C (adversarial):** (1) Product-split reading: 20% (Green-tea flyer) matches the tea-furnace evidence cluster (10–30%, 20–30%, 30%, 34%) because wood-fired tea furnaces already run at ~30–35%; 30–50% (Household flyer) matches the household cluster (traditional 15–20% vs gasifier ≥40–50%). The spread is therefore explained by application, not error. (2) The Brochure's unqualified "một nửa" (50%) sits at the top of the household range and above every tea measurement; the only independent L3 measurement (VNUF 21.9% vs 16.8%) gives 23%. (3) Fuel-switch reading: if GaSIO burns bought pellets (3,000 VND/kg) against free/cheap firewood, the "saving" is negative (−138% to +71%); the claims implicitly assume the same or cheaper feedstock.
**Best evidence level:** L3 (VNUF 2024 efficiency pair, search extract) + L5 project measurements
**New verdict:** Plausible (product-specific): 20% for tea furnaces and 30–50% for household stoves are each supported by the BEST project's own figures and by the efficiency arithmetic; the Brochure's blanket "một nửa" is the upper bound and is Overstated for tea processing (measured 20–34%).
**Confidence:** 0.6 — all project figures are search extracts of self-reported data; the one independent measurement (23%) is below the household claim.
**Change vs prior:** upgraded — from Contradicted to Plausible (product-specific); the prior's "may be product differences" hypothesis is now supported by three independent project statements clustering at 20–34% for tea.
**What CCS could send to settle it:** the VNUF test report (stove model, WBT/ISO protocol, efficiencies), and the kg-wood-per-kg-tea data behind the 20%/34% figures.
**Sources:** [VNUF 2024 gasifier stove paper (search extract)](https://vjol.info.vn/mt/article/view/106721); [SWITCH-Asia VCBG user manual (search extract)](https://www.switch-asia.eu/site/assets/files/4632/3__best_vcbg_user_manual_vnm.pdf); [Oxfam VN node/1219 (search extract)](https://vietnam.oxfam.org/node/1219); [Oxfam story Dinh Hoa (search extract)](https://vietnam.oxfam.org/latest/stories/when-waste-reduces-environmental-pollution-story-dinh-hoa-thai-nguyen); [baothainguyen Dec 2024 Tota furnace (search extract)](https://baothainguyen.vn/kinh-te/202412/lo-dot-cap-nhiet-sach-giam-chi-phi-san-xuat-che-ad808d2); [baothainguyen Feb 2024 firewood price (search extract)](https://baothainguyen.vn/kinh-te/202402/gia-go-keo-tang-f441091/); [Techno Wood 2025 price list (search extract)](https://technowood.vn/bai-viet/bai-viet-chuyen-mon/bang-bao-gia-go-keo-cac-dong-san-pham-go-keo-cua-techno-wood/); [thancuihoangphuong firewood (search extract)](https://thancuihoangphuong.com/gia-cui-kho-dot/); [tiasang Thế Hệ Xanh stove (search extract)](https://tiasang.com.vn/bep-sinh-khoi-hoa-khi-the-he-xanh-tiet-kiem-tren-50-luong-cui-dun-4977017.html)

---

### D5 — Stove price (25 USD household / 60 USD service)
**Quoted (VN):** "Giá: 25 USD/bếp" — Household flyer; "Giá: 60 USD/bếp" — Service-stove flyer
**Prior verdict:** Needs proof (subsidy? fan included?)
**Loop A (direct):** (1) `ccspin.org OR ccs.org.vn bếp khí hóa sinh khối giá bán USD "25 USD" OR "60 USD" ...` → ccspin.org (CCS): "chi phí thấp (từ chỉ $30 cho mỗi bếp nấu)"; "14 mẫu bếp khí hóa gia dụng từ năm 2010"; no 25/60 USD list price found — L6 (search extract). (2) Oxfam ToR node/1149 "Thẩm định giá bếp khí hóa sinh khối liên tục theo thể tích (VCBG) và nhiên liệu sinh khối cho bếp VCBG": the project commissioned an independent appraisal of VCBG stove and fuel prices; result not public — L5 (search extract). (3) Oxfam/CCS 2021 brochure (fetched): micro-enterprise VCBG device "khoảng 3,2 - 8,2 triệu VNĐ" (≈USD 125–320), small-enterprise "130 - 270 triệu VNĐ" — L6. These are processing devices, not cooking stoves.
**Loop B (benchmark):** (1) `Mimi Moto stove price "USD" ... "ACE One" ...` → Engineering for Change (c. 2024): Mimi Moto MSRP USD 33.50, donation price USD 42.51, South Africa retail ZAR 350 ≈ USD 23.63; ACE-1 MSRP USD 165; US camping Mimi Moto USD 119–150 — L5 (search extract). (2) `Mimi Moto stove price USD; ACE One; BioLite HomeStove ...` → BioLite HomeStove USD 40–50 in India/Uganda/Kenya (BioLite statement via Core77) — L6 (search extract). (3) `forced draft biomass stove manufacturing cost bill of materials ...` → energypedia: fan-assisted gasifier stoves "10–110 USD"; improved cookstoves USD 20–85; TEG-stove BOM USD 90 single / USD 68 at 1,000 units with battery USD 2–2.5 — L5/L3 (search extract). (4) `forced draft cookstove cost breakdown ...` → BURN pellet forced-draft stove wholesale ≈USD 50 to PAYG providers; a 2013 forced-draft device USD 102 — L5 (search extract). (5) `bếp khí hóa sinh khối shopee OR lazada ...` and `bếp khí hóa sinh khối giá bán 2025 ...` → no Vietnamese marketplace prices surfaced (null).
**Loop C (adversarial):** (1) Subsidy/ex-works reading: USD 25 ≈ 650,000 VND is below the lowest documented forced-draft retail price (Mimi Moto SA USD 23.6 is a scaled, carbon-financed product), so it is most plausibly an ex-works or project-subsidised price. (2) BOM reading: a basic sheet-steel body plus a 12 V/5 V DC fan (≈USD 1–3 at volume) and a mains adapter (≈USD 2–3) can fit in USD 25 ex-works in Vietnam; a rechargeable battery pack (camping flyer: "có thể sạc lại") would add USD 3–6 and is unlikely to be inside the USD 25. (3) Consistency reading: CCS's own site says "từ $30" (from USD 30) — USD 25 is below CCS's own earlier floor; the service stove at USD 60 is far below the 2021 VCBG micro-device (USD 125–320), so either a different product class or a subsidised price.
**Best evidence level:** L5 (E4C price pages; energypedia range), L6 for CCS's own USD 30
**New verdict:** Plausible — USD 25 and USD 60 are within the documented range for forced-draft gasifier stoves (USD 10–110; Mimi Moto USD 23.6–33.5; BioLite USD 40–50; BURN USD 50 wholesale) and close to CCS's own "từ $30", but it is unclear whether they include fan, power adapter, battery, VAT and distribution margin, or are project-subsidised.
**Confidence:** 0.5 — no CCS price list or the Oxfam price appraisal found; benchmark prices are 2024-era search extracts.
**Change vs prior:** refined — from "Needs proof" to Plausible-with-inclusion-questions; the fan+adapter can fit, a battery probably cannot.
**What CCS could send to settle it:** the current price list with inclusions (fan, adapter, battery, VAT, warranty), ex-works vs retail, and the Oxfam-commissioned VCBG price appraisal report.
**Sources:** [ccspin.org household gasification page (search extract)](https://ccspin.org/index.php/vi/hoa-t-a-ng/ca-ng-ngha-i/267-cong-ngh-1); [Oxfam ToR price appraisal node/1149 (search extract)](https://vietnam.oxfam.org/vi/node/1149); [Oxfam/CCS 2021 brochure (fetched)](https://oi-files-cng-v2-prod.s3.eu-west-2.amazonaws.com/vietnam.oxfam.org/s3fs-public/file_attachments/Brochure%20VCBG%20-%20final.pdf); [E4C Mimi Moto (search extract)](https://www.engineeringforchange.org/solutions/product/mimi-moto/); [E4C ACE-1 (search extract)](https://www.engineeringforchange.org/solutions/product/ace-1-ultra-clean-biomass-cookstove/); [Core77 BioLite HomeStove price (search extract)](https://www.core77.com/posts/57162/A-New-Fire-to-Energy-Device—But-the-UX-May-Need-Some-Help); [energypedia Gasifier Stoves (search extract)](https://energypedia.info/wiki/Gasifier_Stoves); [TEG forced-draft stove BOM, ResearchGate (search extract)](https://www.researchgate.net/publication/318319187_Product_technology_materials_overview_and_economic_aspects_for_development_of_forced_draft_TEG_cookstove); [BURN PAYG stove USD 50 (search extract)](https://giw2017.org/innovations/burn-manufacturing-improved-design-cookstove-pay-you-go-model/); [ScienceDirect forced-draft TEG stove USD 102 (search extract)](https://www.sciencedirect.com/science/article/abs/pii/S0360544214003417)

---

## Summary table

| ID | Prior | New | Level | Confidence | Changed? |
|---|---|---|---|---|---|
| D1 coal 40/50/54% | Contradicted | Contradicted + Overstated at 2025–26 prices (saving −113% to +40% on chips; 50%+ needs residue ≤0.8 M VND/t or 2022 coal prices) | L1 on L6 prices | 0.6 | refined |
| D2 LPG 77/80/85/80–90% | Contradicted | Contradicted (internal; project measured 69%, CCS 2017 said 67%) — each figure individually Plausible (computed 75–92% with chips, 62–82% with pellets) | L5 + L1 | 0.7 | refined (severity down) |
| D3 electricity 10x / 50% | Contradicted (≈3.6x) | Contradicted; "10 lần" Overstated (central 4–8x household, 3–7x production tariff, 1.2–3x tea per BEST) | L1 on L4 tariff + L5 | 0.7 | refined |
| D4 firewood 50% / 30–50% / 20% | Contradicted (product?) | Plausible (product-specific: 20–34% tea, 30–50% household); brochure's blanket 50% Overstated for tea | L3 (VNUF) + L5 | 0.6 | upgraded |
| D5 price 25 / 60 USD | Needs proof | Plausible (within USD 10–110 forced-draft range; CCS site says "từ $30"); inclusions/subsidy unknown | L5/L6 | 0.5 | refined |

**Which CCS figures are supportable, and under what prices (2025–26):**
- Coal: none of 40/50/54% at current domestic cám 5a/6a or Indo GAR-4200 prices unless the biomass is residue at ≤0.8 M VND/t (husk, own-waste chips); with bought pellets GaSIO is 1.5–4x *more* expensive than coal per useful MJ.
- LPG: 77–85% supportable with chips/branches ≤1,500 VND/kg at household LPG prices (34,000–50,000 VND/kg); 77–80% with pellets; "5–10 lần" (80–90%) only at the cheap-residue end; the project's own measurement is 69%.
- Electricity: 50% supportable against resistive heating (actually conservative: 67–93%); "10 lần" only against household tiers 4–6 with 73% stove efficiency and ≤1,000 VND/kg fuel; not supportable against electric tea roasters (BEST: 19%) or heat-pump dryers.
- Firewood: 20% (tea) and 30–50% (household) supportable; 50% unqualified is the upper bound (independent VNUF pair gives 23%).

---

## Gaps for loop 2
1. **Searches not run (budget exhausted):** (a) Decision 1279/QĐ-BCT production/business tariff table (<6 kV normal hours) to replace the derived 1,896 / 3,008 VND/kWh; (b) any 2026 EVN tariff change (`giá điện mới nhất 2026`); (c) confirm Oxfam node/1219 figures 34% / 69% / 19% and their method (sample size, prices used, dates); (d) Tran Nam / Định Hóa cooperative gas-bill figures (10–15 M VND/month) and the baseline consumption; (e) Clean Cooking Alliance / CLASP stove price database for forced-draft stoves 2024–26; (f) refresh efficiency benchmarks with citable L2/L3 sources (ISO 19867-3 tier table; LPG stove 50–60%; traditional Vietnamese stove 15–20%; small coal boiler 60–75%); (g) VCBG feedstock price paid by BEST tea cooperatives (dăm gỗ băm, VND/kg, 2024).
2. **Fetch-blocked primary sources to open by other means:** SWITCH-Asia VCBG user manual (3__best_vcbg_user_manual_vnm.pdf) and best_impact_sheet.pdf (proxy 403); Oxfam node/1219 and ToR node/1149; EVN tariff page; thanda.net / vietanenergy coal pages; baothainguyen Dec 2024 (Tota furnace — is it CCS?); E4C Mimi Moto page; ccspin.org "từ $30" page; VNUF 2024 paper (vjol 106721) to identify the stove tested.
3. **Null results to retry with other terms:** 2024–26 raw rice-husk price (`giá trấu tại nhà máy xay xát 2025 An Giang/Đồng Tháp`); loose sawdust price; corn-cob price (Sơn La/Hòa Bình); TKV 2025–26 official than cám price decision; Vietnamese marketplace prices for forced-draft biomass stoves (`bếp khí hóa có quạt giá`, `bếp đun viên nén giá`).
4. **Hypotheses to test adversarially:** D1 — whether CCS's 54% derives from 2022 coal prices (Indo GAR 4200 ≥2.5 M VND/t); D5 — whether USD 25 is the BEST-project subsidised or ex-works price and whether a battery is included (camping flyer says rechargeable).
5. **CCS documents that would settle Group D:** the BEST "standard cost-benefit calculation" study; fuel-per-kg-tea measurements (LPG, electricity, wood, VCBG) with dated prices; current price list with inclusions; the Oxfam-commissioned VCBG price appraisal.

### Fetch failures logged this loop (ENOTFOUND unless noted)
vietnam.oxfam.org; www.switch-asia.eu (proxy 403 policy); thoibaotaichinhvietnam.vn; luatvietnam.vn; kinhdoanhthannhapkhau.com; vietanenergy.com.vn; baothainguyen.vn (×2); thancuihoangphuong.com; nld.com.vn; naangroup.com; hex-boilers.com; congnghevietphat.com; www.engineeringforchange.org; moit.gov.vn; thuvienphapluat.vn; ccspin.org; tietkiemnangluong.com.vn; tiasang.com.vn; thanda.net; chogia.vn; www.evn.com.vn. Successful: Oxfam S3 brochure PDF (text extracted with pdftotext).
