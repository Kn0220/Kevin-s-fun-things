# Claims verification protocol (read fully before starting)

## Purpose
Re-verify every factual claim in CCS Vietnam's eight GaSIO / VCBG brochures (Vietnamese PDFs, Apr–Sep 2025) against the latest independent evidence (2024–2026 reports, peer-reviewed papers, standards, patent databases, government statistics). An earlier pass produced provisional verdicts (below). Your job is to CONFIRM, OVERTURN or REFINE each one with better evidence, and to log every search attempt.

## Framework

### Evidence level (grade the best source you find for each claim)
- **L1** Physical law or arithmetic (stoichiometry, unit analysis) — cannot be argued with.
- **L2** Standards body or intergovernmental default (ISO 19867 / ISO/TR 19867-3 tiers, IPCC 2019 Refinement biochar appendix, WHO, IEA, UN agencies).
- **L3** Peer-reviewed paper (journal, DOI).
- **L4** Accredited third-party lab report, national statistics office, government decree, patent-office record.
- **L5** Reputable NGO / industry report (Clean Cooking Alliance, ESMAP, IRENA, Puro.earth, CDR.fyi, Carbon Pulse, Nitidae, GIZ, SWITCH-Asia), established press.
- **L6** Company marketing, vendor listings, blogs, unsourced web pages.

### Verdict scale (pick one per claim)
- **Confirmed** — independent L1–L4 evidence supports the claim as stated.
- **Plausible** — consistent with L2–L5 evidence but no direct proof for GaSIO itself.
- **Overstated** — the claim exceeds what evidence supports, by a stated factor or range.
- **Contradicted** — the claim conflicts with another CCS document or with L1–L4 evidence.
- **Impossible** — violates L1 (physics/arithmetic).
- **Unverifiable** — three loops found no evidence either way (see loop rule).

### Confidence (0.0–1.0) in your verdict, with one sentence why.

### The three-loop rule (mandatory)
For EVERY claim, run at least three distinct search loops before concluding "nothing found" or settling a verdict:
- **Loop A — direct:** search the claim's own terms (English AND Vietnamese where relevant), the product name (GaSIO, VCBG, "khí hóa sinh khối liên tục theo thể tích", CCS, ccs.org.vn, ccspin.org, Nguyễn Hồng Long), and the partner names (Oxfam, SWITCH-Asia BEST, CREEC, USTH, Vietnam Forestry University, TU Delft).
- **Loop B — benchmark:** search for the independent benchmark the claim should be compared with (ISO tier tables, IPCC tables, peer-reviewed measurements of comparable stoves/chars/boilers, national statistics). Prefer 2024–2026 sources; use `WebSearch` mode "extended" when standard results are thin.
- **Loop C — adversarial:** search for evidence that would make the claim TRUE under some reading you have not considered (different test protocol, different basis, different baseline fuel, typo hypothesis), and for evidence that would make the earlier verdict WRONG.
Log each loop in your notes (query used, what came back, source level). If a loop finds nothing, say so explicitly — a logged null result is a finding.

### Source handling
- Open the page with `WebFetch` whenever possible; if fetch is blocked, say "(search extract)" next to the citation.
- Never invent a DOI, patent number, page number or figure. If you can't verify, write "not found" and what you tried.
- Separate CCS's own statements (L6) from independent evidence.
- Date every figure.

## Output format (per claim)
```
### <ID> — <short claim>
**Quoted (VN):** "<exact Vietnamese phrase>" — <file>, <page>
**Prior verdict:** <from the list below>
**Loop A (direct):** <query> → <result + source + level>
**Loop B (benchmark):** <query> → <result + source + level>
**Loop C (adversarial):** <query> → <result + source + level>
**Best evidence level:** L_
**New verdict:** <Confirmed/Plausible/Overstated/Contradicted/Impossible/Unverifiable>
**Confidence:** 0.__ — <why>
**Change vs prior:** <none / upgraded / downgraded / refined> — <one line>
**What CCS could send to settle it:** <document or data>
**Sources:** <markdown links>
```
End your file with a "Summary table" (ID | prior | new | level | confidence | changed?) and a "Gaps for loop 2" list.

## The CCS files (Google Drive; links open the PDF)
- Brochure: https://drive.google.com/file/d/1UIqUVvTTx2fiHVLRdSewam3lkjenB7XD/view
- Overview ("2. Giới thiệu GaSIO", 18 pp, page numbers printed at bottom): https://drive.google.com/file/d/1vX1mth_3_Gw-4GQVPwFlbB3UOVpn3NA3/view
- Household flyer: https://drive.google.com/file/d/1aJQ93N61-P_Us646Dm1sPjFyy8NfbsqW/view
- Service-stove flyer: https://drive.google.com/file/d/1LxRc9KjiQvQqN6hok4ZQ5Hcu1v22OjUv/view
- Green-tea flyer: https://drive.google.com/file/d/1bfJwIYV7wWtCizlbIDy7Ak8olaEKrA7C/view
- Industrial tea flyer: https://drive.google.com/file/d/1Q70L5B_nheHOExZWmXBLYpSqTjdhIG31/view
- Camping-stove flyer: https://drive.google.com/file/d/14uMAsxgRb3loajvH-yDcwUkLUExMHJYy/view
- Boiler flyer: https://drive.google.com/file/d/1bx5Dz2-AJyiomqtRg34u69y9ZrCegVr4/view
(You cannot download these from this environment; the quotes below are verbatim extracts already taken from them.)

## Claims and prior verdicts

### Group A — Biochar and carbon storage
- **A1** Service-stove flyer: "1 kg than sinh học giúp chôn xuống đất 5,6kg cacbonic". Prior: **Impossible** (max 44.009/12.011 = 3.664 kg CO2 per kg C).
- **A2** Household flyer + Overview p.3: "1kg than sinh học giúp chôn xuống đất 3,5kg cacbonic". Prior: **Overstated** (0.95×3.664=3.48 theoretical gross ceiling; IPCC 2019 defaults for gasification char: Fc rice husk/straw 0.14, wood 0.52; Fperm 0.65/0.80/0.89 → 0.33–1.70 kg CO2/kg).
- **A3** Overview p.4: "Hàm lượng cacbon cố định trong than sinh học là 95%" (USTH analysis 2024). Prior: **Overstated** (rice-husk char typically 20–40% ash, 34–69% fixed carbon; 95% only dry-ash-free woody char).
- **A4** Overview p.2: "Trên thị trường quốc tế, than sinh học có thể được bán với giá cao (8 triệu đồng/tấn), cao hơn 4 - 5 lần so với đầu vào sinh khối". Prior: **Wrong label** (8M VND/t ≈ USD 300/t is a domestic Vietnamese list price, BiocharVN).

### Group B — Lab performance and specifications
- **B1** Overview p.4: ISO 19867-1:2018 test by CREEC (Uganda, ISO/IEC 17025): Tier 5 efficiency, durability, safety, CO; Tier 4 PM2.5. Prior: **Plausible, needs proof** (matches Mimi Moto; report not public).
- **B2** Overview p.1: "Hiệu suất tối đa của bếp dân sinh là 83,7%". Prior: **Overstated** (ISO Tier 5 ≥50%; best tested biomass stoves 44–53%).
- **B3** Brochure: "Bếp đạt chứng nhận theo tiêu chuẩn ISO 19867-1:2018". Prior: **Risky wording** (ISO 19867-1 is a test method, not a certification).
- **B4** Overview p.2: "Không tạo ra chất độc hại trong quá trình đốt". Prior: **Risky wording** (Tier 4 PM2.5 ≤62 mg/MJd is low, not zero).
- **B5** Overview p.3 "Từ 1 đến 6 kW" vs Household flyer "0,5 - 10 kW". Prior: **Contradicted**.
- **B6** Overview p.3: "đun sôi 1 lít nước trong 2 phút". Prior: **Plausible** (≈2.6 kW into water).
- **B7** Overview p.5: "Độ bền tối thiểu của bếp 25,2 tháng vận hành" (Vietnam Forestry University) vs "Tuổi thọ 10 năm". Prior: **Contradicted**.
- **B8** Overview p.1 "lên đến 73%" vs ~75% (MOIT/DANIDA 2016 on ccspin.org). Prior: **Contradicted (minor)**.
- **B9** Overview p.7 (bamboo-shoot unit): "Công suất ước tính: 0.63 kW/h", "Điện tiêu thụ quạt: 1.1kW/h"; also p.5 "65 Wh/h". Prior: **Wrong (unit error)**.

### Group C — CO2 reduction figures
- **C1** Overview p.2 "Ước tính 1.027 kg CO2 được giảm thiểu mỗi năm nếu sử dụng bếp khí hóa"; p.3 "Giảm khoảng 8 tấn CO2 trong vòng đời sản phẩm"; Household flyer "3 - 5 tấn/bếp/năm; và 30 - 50 tấn/bếp/vòng đời (10 năm)". Prior: **Contradicted** (5x gap; 1.027×10=10.3≠8).
- **C2** Service-stove flyer: "4,5 - 7,5 tấn/bếp/năm". Prior: **Needs proof**.
- **C3** Overview p.5 (green-tea unit) "Lượng cacbonic giảm được trong suốt vòng đời sản phẩm khoảng 1,5 tấn" vs Green-tea flyer "Giảm CO₂: 12 tấn/năm/thiết bị". Prior: **Contradicted** (80x).
- **C4** Overview p.12 (hybrid solar dryer, 75 kW–1 MW): "khoảng 15 tấn" lifetime. Prior: **Contradicted/low**.
- **C5** Overview p.7–9: "2,2 tấn CO2/tấn măng khô", "2,1 tấn CO2/tấn sản phẩm" (herbs), "2,2 tấn CO2/tấn sản phẩm" (bánh chưng). Prior: **Needs proof**.
- **C6** Industrial tea flyer: "Giảm CO₂: 2.800 tấn/năm" for a 1,000 t/yr tea line replacing coal, using 1,500 t biomass. Prior: **Plausible** (≈1.1 kg coal/kg tea).
- **C7** Camping flyer: "720 gram CO2" saved per meal; "Hoạt động bằng pin, có thể sạc lại", "Thời gian nấu liên tục: Không giới hạn". Prior: **Needs proof**.

### Group D — Fuel-cost savings and price
- **D1** Saving vs coal: Overview p.2 "Tiết kiệm đến 40% chi phí nhiên liệu so với sử dụng than đá" vs p.6 "Giảm 50% so với sử dụng than" vs p.14 "Tiết kiệm 54% chi phí so với dùng than". Prior: **Contradicted**.
- **D2** Saving vs LPG/gas: Overview p.2 "80% chi phí so với đốt bằng LPG hoặc dầu"; p.14 "Tiết kiệm 77% chi phí so với dùng Gas"; Brochure "chi phí chỉ bằng 15% so với sao chè bằng LPG"; Household flyer "05 - 10 lần so với đun bằng gas". Prior: **Contradicted**.
- **D3** Saving vs electricity: Brochure "rẻ hơn 10 lần so với đun bằng điện" vs Green-tea flyer / Overview p.12 "Giảm 50% so với sử dụng điện". Prior: **Contradicted** (rough check ≈3.6x).
- **D4** Saving vs firewood: Brochure "giá bằng một nửa so với đun củi"; Household flyer "30% - 50% so với đun củi"; Green-tea flyer "Giảm 20% so với sử dụng củi". Prior: **Contradicted (may be product differences)**.
- **D5** Household flyer "Giá: 25 USD/bếp"; Service flyer "Giá: 60 USD/bếp". Prior: **Needs proof** (subsidy? fan included?).

### Group E — Scale and track record
- **E1** Boiler flyer + Overview p.13: boilers "từ 20 kg hơi nước một giờ đến các lò có công suất 20 tấn hơi nước một giờ" vs Overview p.6 industrial "300 kW - 3MW". Prior: **Contradicted** (20 t/h ≈ 14.9 MW).
- **E2** Brochure: "1000+ Các doanh nghiệp siêu nhỏ, nhỏ và vừa được chuyển giao các công nghệ sạch". Prior: **Needs proof**.

### Group F — Market and health figures
- **F1** Overview p.2: "Gần 75% nhiên liệu tiêu thụ ở Việt Nam là nhiên liệu hóa thạch, thải ra trên 1,7 triệu tấn CO2/năm". Prior: 75% **Confirmed** (EI 2024 ≈77%); 1.7 Mt **Wrong** (actual ≈300–390 Mt).
- **F2** Overview p.2: "Tổng lượng phế phụ phẩm Việt Nam là 160 triệu tấn, trong đó khoảng 65 triệu tấn phụ phẩm nông, lâm nghiệp đang bị đốt, thải bỏ, tiềm năng kinh tế là 24 triệu TOE (tương đương với 28 tỷ USD) (2022)". Prior: **Needs a source** (published crop residues 79–98 Mt).
- **F3** Household + Service flyers: "ô nhiễm khói bếp là nguyên nhân khiến 2 triệu người chết mỗi năm" (WHO). Prior: **Outdated** (WHO: 3.2M for 2020, 2.9M for 2021).
- **F4** Household flyer: "Tại Việt Nam, khoảng 60.000 ca tử vong hàng năm là do ô nhiễm không khí". Prior: **OK as worded** (WHO all air pollution).

### Group G — Patents and naming
- **G1** Brochure: "Bằng độc quyền sáng chế Phương pháp và Thiết bị Khí hóa Sinh khối, tại Việt Nam, năm 2023"; "Bằng độc quyền giải pháp hữu ích Bếp Khí hóa sinh khối dân sinh, tại Việt Nam, năm 2017"; "Bằng sáng chế bếp dân sinh sử dụng công nghệ khí hóa sinh khối liên tục theo thể tích, tại Đan Mạch, năm 2020"; Overview p.18: two "Đăng ký sáng chế" (applications). Prior: **Unverified** (no number found anywhere).
- **G2** "Khí hóa sinh khối liên tục theo thể tích" = Volumetric vs Oxfam ToR "Vertical Continuous Biomass Gasification". Prior: **Contradicted (naming)**.
- **G3** Awards: "Giải thưởng Ý tưởng Tương lai Bền vững" (2015, with TU Delft), Vietnam Climate Innovation Center award, Danish start-up programme, Mekong Startup 2022, VTV 2015. Prior: **Unverified**.
