# Competitive Landscape: Biomass Gasifier / Forced-Draft / Biochar Cookstoves vs CCS Vietnam GaSIO (2025–2026)

Research note: researched October 2026. WebFetch failed with DNS errors for most target domains (cleancooking.org, ccspin.org, moit.gov.vn, vnexpress.net, mimimoto.nl), so most findings below come from search-result extracts of the cited pages rather than full-page reads. Where a figure appeared only in a snippet, treat it as provisional. GaSIO figures are company claims from CCS brochures (2025) unless stated otherwise; no third-party copy of the CREEC Uganda test report was found online.

## 1. ISO 19867-3 tier thresholds, and where GaSIO's claimed Tier 5 / Tier 4 sits

### Takeaway
On the ISO/TR 19867-3:2018 default scale, GaSIO's claimed results (Tier 5 efficiency ≥50%, Tier 5 CO ≤3.0 g/MJd, Tier 4 PM2.5 ≤62 mg/MJd) would put it level with the best published biomass stoves, such as Mimi Moto. They would not put it above them: Tier 5 PM2.5 (≤5 mg/MJd) is in practice out of reach for solid biomass, and Tier 4 PM2.5 is the realistic ceiling.

### Cited Findings
- ISO/TR 19867-3:2018 default lab tiers (from a Clean Cooking Alliance summary of the ISO TR). Thermal efficiency: T5 ≥50%, T4 ≥40%, T3 ≥30%, T2 ≥20%, T1 ≥10%, T0 <10%. CO (g/MJd): T5 ≤3.0, T4 ≤4.4, T3 ≤7.2, T2 ≤11.5, T1 ≤18.3, T0 >18.3. PM2.5 (mg/MJd): T5 ≤5, T4 ≤62, T3 ≤218, T2 ≤481, T1 ≤1030, T0 >1030 — [Clean Cooking Alliance doc](https://cleancooking.org/wp-content/uploads/2021/07/626-1-1.pdf); [ISO/TR 19867-3:2018](https://www.iso.org/standard/73935.html); [WHO, Setting national voluntary performance targets](https://www.who.int/publications/i/item/9789240023987)
- Tier 5 PM2.5 and CO correspond to the emission rates most likely to meet WHO guideline levels. ISO/TR 19867-3 is a technical report (voluntary targets), not a normative standard, and the default values can be adjusted to local conditions — [Clean Cooking Alliance doc](https://cleancooking.org/wp-content/uploads/2021/07/626-1-1.pdf)
- Under the ISO framework, each metric is tiered separately and the tiers cannot be combined into one overall tier. Results from other protocols (for example WBT/IWA) cannot be mapped onto the ISO tiers — [Clean Cooking Catalog, ACE One page](https://catalog.cleancooking.org/stove_details.html?stove_id=stove_0CBX51V)
- Best published biomass benchmark: Mimi Moto (forced-draft pellet gasifier) is reported at ISO Tier 5 thermal efficiency (50%), Tier 5 CO, and Tier 4 PM2.5 — [Clean Cooking Alliance innovation page](https://cleancooking.org/innovations/clean-burning-gasification-stove/). Mimi Moto's own site says EPA testing under ISO 19867-3 gave Tier 5 efficiency and CO and "high Tier 4" PM2.5 — [mimimoto.nl/products](https://mimimoto.nl/products/)
- The Apeli forced-draft stove (peer-reviewed, modified ISO 19867-1 method) reached 44.1% efficiency at high power on pellets: Tier 4 efficiency and PM2.5, Tier 5 CO — [Energies 2023, 16(7):3278](https://www.mdpi.com/1996-1073/16/7/3278)
- A forced-draft TLUD prototype in Mexico (P3-Chupiri) is reported at ISO/TR 19867-3 Tier 5 for thermal efficiency, fuel savings, and indoor emissions — [Sustainable Energy Technologies and Assessments 2024](https://www.sciencedirect.com/science/article/abs/pii/S2213138824002091)
- In field use, Mimi Moto in Rwanda reached about Tier 3–4 for CO and PM. Lab emissions were lower than high field emissions, and refuelling caused the largest and most variable emission spikes — [Atmosphere 2019, in-home emissions](http://dx.doi.org/10.3390/atmos10050290); [PMC11973569](https://pmc.ncbi.nlm.nih.gov/articles/PMC11973569)

### Inferences
- GaSIO's claimed tier profile (T5 efficiency / T5 CO / T4 PM2.5 / T5 safety / T5 durability) matches the published profile of Mimi Moto, which is generally treated as the cleanest commercial biomass stove. If CREEC's report confirms it, GaSIO would be in the top group, not uniquely better. Tier 5 durability and safety are a plus, since many competitors only report emissions and efficiency.
- The finding that refuelling drives emission spikes matters for GaSIO. A continuous-feed design could in principle avoid the batch-reload spikes that hurt Mimi Moto and TLUDs in the field. Equally, continuous top-up of loose residues could create its own spikes. This is a testable differentiator worth asking CCS about: did CREEC measure emissions across a feeding event?
- Because ISO tiers are reported per metric and per test, "Tier 5" claims should come with the CREEC report number, the fuel tested (pellets vs rice husk), and the power level. Gasifier results usually depend strongly on fuel.

### Gaps
- No public copy of the CREEC Uganda ISO 19867-1 report for GaSIO was found, so the fuel used, the char-credit treatment, and the actual numeric values are unknown.
- The Clean Cooking Catalog could not be fetched (DNS failure), so I could not get a full list of stoves with ISO Tier 5 PM2.5. From the literature, Tier 5 PM2.5 is generally reached only by LPG, ethanol, biogas, and electric stoves, but no catalog query confirmed this.

## 2. Is the 83.7% maximum thermal efficiency plausible?

### Takeaway
Not as a standard ISO 19867-1 cooking-efficiency figure. The best biomass stoves in published lab tests reach roughly 40–53%. The 83.7% is most likely a char-credited efficiency, a gasifier "cold gas" or system efficiency, a non-ISO protocol result, or a peak/high-power point. Using it in investor or carbon materials without a clear definition carries credibility risk.

### Cited Findings
- Published highs: a mini pellet forced-draft stove reached up to 47% in a WBT — [S2590174526001558](https://www.sciencedirect.com/science/article/pii/S2590174526001558); Apeli reached 44.1% — [MDPI Energies](https://www.mdpi.com/1996-1073/16/7/3278); a natural-draft pellet TLUD (StoveTec) reached 53%, against 32% for the Oorja forced-draft stove — review cited via [search on gasifier efficiency literature](https://www.researchgate.net/publication/365485054_A_review_of_thermal_efficiency_and_optimal_design_for_biomass_gasifier-stove); Mimi Moto is reported at 50% — [CCA](https://cleancooking.org/innovations/clean-burning-gasification-stove/), but 46.8% in another listing — [Engineering for Change, Mimi Moto](https://www.engineeringforchange.org/solutions/product/mimi-moto/); BioLite HomeStove 36.9% — [E4C](https://www.engineeringforchange.org/solutions/product/biolite-homestove); ACE-1 41.5% (2015) — [E4C ACE-1](https://www.engineeringforchange.org/solutions/product/ace-1-ultra-clean-biomass-cookstove/)
- ISO 19867-1 requires that, for solid-fuel stoves that produce char, thermal efficiency is reported both with and without energy credit for the char. It defines "char energy efficiency" (energy of char produced / energy of fuel fed) as a separate metric — [ISO 19867-1:2018 preview (SIS)](https://www.sis.se/api/document/preview/80004551/); [ISO OBP](https://www.iso.org/obp/ui/#iso:std:iso:19867:-1:ed-1:v1:en)
- The char credit changes the figure substantially. In an Aprovecho/OSTI forced-jet retrofit study, efficiency improved 34% when calculated without the char energy credit, against 21% with it, so the two methods give materially different numbers — [OSTI 2418490](https://www.osti.gov/servlets/purl/2418490)
- Belonio's 19 kW continuous-flow rice-husk gasifier reported 63% "overall efficiency", while the household continuous-flow rice-husk stove was only about 21% thermal efficiency (boils 2 L in 14 min). Efficiency definitions and scales clearly differ — [Belonio, Continuous-Flow Rice Husk Gasifier (bioenergylists)](https://stoves.bioenergylists.org/files/Continuous-Flow%20Rice%20Husk%20Gasifier%20for%20Small%20Scale%20Thermal%20Applications.pdf); [Household continuous-flow rice husk gas stove](https://stoves.bioenergylists.org/node/2962)

### Inferences
- Likely explanations for 83.7%, from most to least likely:
  1. A char-credited efficiency, in which the energy left in the ~95%-fixed-carbon biochar is subtracted from the input. For a char-making stove this can inflate the figure a lot.
  2. A gasifier conversion ("cold gas") or combined heat-plus-char energy efficiency, not heat delivered to the pot.
  3. A large-pot, high-power, or space-heating measurement, or a non-ISO protocol.
  4. A test-day maximum, not the ISO weighted average.
- A stove that makes biochar is by design leaving 15–30% of the fuel energy in the char. A true pot efficiency above 80% on the fuel actually fed is physically implausible for an open-pot biomass stove: heat transfer to a pot alone usually caps open-flame stoves around 50–60%.
- Recommendation for the report: ask CCS for both ISO figures (with and without char credit) and the char energy efficiency, and present Tier 5 (≥50%) rather than 83.7%.
- "Boils 1 L in 2 min" works out to roughly 2.6 kW of net heat to the water (about 335 kJ to heat 1 L by 80 °C, over 120 s). That is plausible at the top of a 1–6 kW stove's range, and consistent with a high-power phase.

### Gaps
- The CREEC report's efficiency definition for the 83.7% figure is not known.
- No peer-reviewed paper on VCBG/GaSIO was found.

## 3. Competitor profiles (technology, fuel, power, price, tiers, volumes, business model)

### Takeaway
The main competitors are well-funded African forced-draft pellet or wood stoves (Mimi Moto/SupaMoto, ACE, BioLite) and charcoal efficient stoves (BURN). They compete on scale (tens of thousands to millions of units), carbon-credit finance, and PAYGo or fuel-subscription models, not on fuel flexibility. Few of them make biochar, and none advertises continuous feeding of loose, unprocessed residues. That is GaSIO's niche, and continuous-flow rice-husk designs (Belonio, Philippines) are the closest technical analogue.

### Cited Findings

**Emerging Cooking Solutions / Mimi Moto (Netherlands/Zambia), with SupaMoto**
- Forced-draft (fan) micro-gasifier, primarily pellet-fuelled. Reported ISO tiers: Tier 5 efficiency (50%), Tier 5 CO, Tier 4 PM2.5 — [CCA](https://cleancooking.org/innovations/clean-burning-gasification-stove/); E4C reports 46.8% efficiency and CO 0.154 g/MJd — [E4C](https://www.engineeringforchange.org/solutions/product/mimi-moto/)
- 68,000 units sold in 23 countries in sub-Saharan Africa and SE Asia as of May 2023. Sold to pellet companies at about USD 45–60 per stove depending on spec and volume; E4C lists a suggested retail price of USD 33.50 — [CCA profile](https://cleancooking.org/?p=11063); [E4C](https://www.engineeringforchange.org/solutions/product/mimi-moto/)
- Business model is fuel-as-a-service: pellet subscriptions are bundled with the stove (SupaMoto, Zambia; 20,000-household scale-up planned). Fuel sales data make it eligible for metered carbon methodologies, which give "higher quality carbon credits and better prices per tonne". The claimed saving is 4–5 tCO2 per stove per year — [CCA profile](https://cleancooking.org/?p=11063)
- Zambia study: 37% of MimiMoto households used it as their primary stove and 41% as a secondary stove. Users burned 1.1 kg/day less charcoal — [UNC ZCCS brief](https://eppsa.cpc.unc.edu/wp-content/uploads/2021/06/ZCCS-SupaMoto-Brief-FINAL.pdf)
- Does not produce biochar as a co-product. Pellet fuel requires a pellet supply chain.

**Inyenyeri (Rwanda)**
- Leased the Mimi Moto fan gasifier free in exchange for buying the company's wood pellets (pellet suggested retail price USD 6.50, circa 2018) — [E4C Inyenyeri](https://www.engineeringforchange.org/solutions/product/inyenyeri-fuel-pellets/); [Kigeme refugee camp social impact assessment](https://cleancooking.org/reports-and-tools/inyenyeri-clean-cooking-pilot-in-kigeme-refugee-camp-social-impact-assessment/)
- Successor: BioMassters (a Rwandan pellet company founded in 2020) is led by former Inyenyeri staff — [CCA BioMassters interview](https://cleancooking.org/news/biomassters-a-tailored-approach-with-vast-potential/)

**African Clean Energy (ACE One / ACE 2), Lesotho/Uganda/Cambodia**
- Forced-draft biomass stove with an integrated solar panel and battery that powers the fan and charges phones and lamps. Burns wood, dung, and crop residues (batch top-up). ACE-1 efficiency was 41.5% (2015 data). An E4C summary gives IWA/ISO "tier 3 emissions, tier 3 efficiency, tier 4 safety" — [E4C ACE-1](https://www.engineeringforchange.org/solutions/product/ace-1-ultra-clean-biomass-cookstove/); the Clean Cooking Catalog has an ACE One entry, but ISO values could not be read — [Catalog](https://catalog.cleancooking.org/stove_details.html?stove_id=stove_0CBX51V)
- Price: USD 140 cash or USD 150 on instalments (SWITCH-Asia case, Cambodia); suggested retail price USD 165 — [SWITCH-Asia ACE case](https://switch-asia.eu/site/assets/files/4046/ace.pdf); [E4C](https://www.engineeringforchange.org/solutions/product/ace-1-ultra-clean-biomass-cookstove/)
- Collects usage data from each stove to support carbon credits; claims 2–3 tCO2 per stove per year. A project closed in February 2025 after about 12,000 tCO2 saved — [SWITCH-Asia](https://switch-asia.eu/site/assets/files/4046/ace.pdf); [Nature Network 2025](https://www.the-nature-network.com/en/?p=1174)
- ACE is notable as an existing PAYGo forced-draft biomass seller in Cambodia (SE Asia), a direct regional reference for GaSIO.

**BioLite (USA): HomeStove, CampStove 2+, FirePit+**
- HomeStove: thermoelectric-powered fan, wood. E4C lists 36.9% efficiency, PM "unknown", suggested retail price USD 60. Claimed 90–95% smoke reduction and 91% CO reduction (manufacturer or secondary claims). Carbon offsets via Gold Standard credits subsidise the price — [E4C HomeStove](https://www.engineeringforchange.org/solutions/product/biolite-homestove); [BioLite Wikipedia](https://en.wikipedia.org/wiki/BioLite); [REI blog](https://www.rei.com/blog/camp/good-gear-biolite-fuels-outdoor-adventures-and-off-grid-households)
- CampStove 2+ (see section 4): about USD 150, boils 1 L in 4.5 min, 3,200 mAh battery — [Trailspace](https://trailspace.com/gear/biolite/campstove-2+)

**BURN Manufacturing (Kenya): Jikokoa (charcoal) and Kuniokoa (wood)**
- Over 5.2 million biomass, LPG, and electric appliances sold since 2011 (May 2025). Several projects were on track for ICVCM Core Carbon Principles (CCP) labels in 2025, which would be among the first CCP-labelled cookstove credits — [BURN newsroom](https://burnstoves.com/media/newsroom/newsroom-1)
- Stove price targets (2022): USD 15–25 for Jikokoa and USD 0–10 for Kuniokoa, enabled by carbon finance — [Giving Green](https://www.givinggreen.earth/research/burn)
- Relevance: a charcoal substitute, not a gasifier. It shows the "carbon-subsidised near-free stove" price benchmark that GaSIO's USD 25 must compete against in carbon-financed markets.

**Wider carbon-finance context**
- An AP story (September 2026) cites a distributor of more than 7.3 million stoves in 11 African countries, and an efficient biomass stove normally retailing at about USD 40 selling for as little as USD 5 after carbon subsidies — [ABC/AP](https://abcnews.com/Business/wireStory/carbon-credit-financing-emerges-africas-biggest-bet-expanding-136247673)
- As of August 2025, cookstove projects had issued more than 181 million credits. RMI flags monitoring as a high-concern quality risk (survey-only methods can over-count usage) — [RMI technical explainer](https://rmi.org/resources/technical-explainer-clean-and-improved-cookstove-carbon-credits/)
- A planning calculator gives about 2.5–3.5 tCO2e per household per year for gasifier/TLUD stoves, at credit prices of about GBP 10–18/t (indicative only) — [Carbon Workbench calculator](https://thecarbonworkbench.com/cookstove-calculator)

**TLUD and biochar-producing stoves**
- PowerPellet TLUD-ND (natural-draft) in Kenya, advised by Paul "Dr TLUD" Anderson. Biochar Pamoja handles training, maintenance, pellet supply, and sale of carbon removal (CDR) credits to fund more stoves. Stoves are owned by women's groups — [woodgas.com project doc, Jan 2024](https://woodgas.com/wp-content/uploads/2024/01/PowerPellet-TLUD-ETHOS-2024-01-26.pdf)
- Kenya field trial of biochar-producing TLUD/gasifier stoves (GASTOV) in 150 households (Embu, Kwale, Siaya): up to 82% CO and 97% PM2.5 concentration reductions against three-stone fires. Biochar from cookstoves reduced on-farm GHG emissions — [Mitig Adapt Strateg Glob Change 2020](https://link.springer.com/article/10.1007/s11027-020-09920-7)
- Exomad Green (Bolivia) is a large industrial biochar carbon-removal producer under the Puro.earth methodology (CORCs, Sylvera AA, offtakes with Microsoft for 1.24 Mt and Supercritical for up to 500 kt). No cookstove product was found; it is a kiln/plant-scale competitor for biochar credit buyers, not a stove maker — [ESG Today](https://www.esgtoday.com/exomad-green-supercritical-sign-500000-ton-biochar-carbon-removal-agreement/); [Commons](https://thecommons.earth/blog/commons-offset-portfolio-exomad-green); [Argus](https://www.argusmedia.com/de/news-and-insights/latest-market-news/2698805-exomad-green-starts-building-bolivian-biochar-plant)

**Continuous-flow rice-husk gasifiers (Philippines, Belonio / Central Philippine University)**
- The household continuous-flow rice-husk gas stove has about 21% efficiency (boils 2 L in 14 min) and costs PHP 2,000–2,500 (about USD 36–45 at 55 PHP/USD; historical figures). A 19 kW continuous-flow gasifier has 63% "overall efficiency" and costs PHP 35,000, with a payback under one year against LPG. A 2010 paper gives PHP 1,500 per kWt — [Household continuous-flow stove](https://stoves.bioenergylists.org/node/2962); [19 kW gasifier](https://stoves.bioenergylists.org/node/1159); [CF gasifier for thermal applications](https://stoves.bioenergylists.org/node/2878)
- These are the closest prior art to "volumetric continuous biomass gasification" with loose rice husk. They show the concept is not new, but the household continuous-flow version historically had low efficiency.

**Vietnam: domestic competitors and substitutes**
- CCS's own continuous-gasifier R&D (late 2016): five lab prototypes of a continuous-feed stove, refuelling in 15-minute cycles, gas within about 1 minute of lighting, gas quality better than CCS's batch stoves. Five gasification stoves were also built for a community project in Gia Lam, Hanoi — [CCS update](http://www.ccspin.org/index.php/en/news-information/303-update-on-continuous-gasifier-r-d-progress)
- The BEST project (Oxfam and CCS, EU-funded, 2020–2024) in Thai Nguyen, Lao Cai, Tuyen Quang, and Yen Bai targeted about 2,500 agri-processing households and small enterprises with biomass gasification equipment. The Ministry of Industry and Trade (MOIT) notes biomass devices exist on the market but are not widely adopted, mainly for lack of models suited to local finances — [MOIT article (via search extract)](https://moit.gov.vn/bao-ve-moi-truong/giai-phap-nang-luong-ben-vung-cho-che-bien-nong-san-va-quan-.html); [Thanh Tra, SPIN project gasification breakthrough](https://thanhtra.com.vn/kinh-doanh-A08BE54D6/du-an-spin-buoc-dot-pha-cong-nghe-khi-hoa-F3FCD0EC.html)
- Other Vietnamese biomass gas stoves: a Vietnamese-invented "bếp ga sinh học" (biomass gas stove) using rice husk and corn cobs sold for about VND 1.8 million (about USD 70; circa 2018) — [VnExpress](https://vnexpress.net/bep-ga-sinh-hoc-tan-dung-vo-trau-loi-ngo-3772018.html); a gasification-chamber improved wood stove from HCMC University of Technology students claims 45% fuel saving — [Tuoi Tre](https://tuoitre.vn/bep-cui-bao-ve-moi-truong-1291370.htm); a 2024 Vietnam Forestry University study on household biomass gasifier stoves ("bếp dân sinh") — [JVE / qucosa](https://journals.qucosa.de/jve/article/download/71/70); home-made rice-husk stoves cost under VND 200,000 (about 1 kg husk per 45–50 min burn) — [Bao Dong Nai](https://baodongnai.com.vn/netdepdoithuong/201301/chiec-bep-dun-trau-huu-dung-2215394/)
- Low-end "improved wood stoves" (bếp củi cải tiến) sell for about VND 160,000–240,000 (about USD 6–10) online (Huong Giang 40 cm, Tuyen Cuong) — [Hugiasmart](https://www.hugiasmart.vn/collections/bep-cui-cai-tien-huong-giang); [Bigomart/Sendo](https://bigomart.info/s2-product/sendo/bep-cui-tiet-kiem-17001800)
- Rice husk resource: about 8 Mt per year in Vietnam, largely unused — [MOIT/Tap chi Cong Thuong (via search extract)](https://tapchicongthuong.vn/khi-hoa-nhien-lieu-sinh-khoi-giai-phap-bao-ve-moi-truong-ben-vung-15752.htm)
- The "Hoàng Cầm stove" and "lò trấu" (traditional rice-husk stove) have Wikipedia entries, showing a long tradition of rice-husk stoves in Vietnam — [Lò trấu](https://en.wikipedia.org/wiki/L%C3%B2_tr%E1%BA%A5u)

### Inferences
- **Price.** GaSIO's USD 25 is cheaper than the unsubsidised forced-draft leaders (ACE USD 140–165, Mimi Moto USD 33–60 wholesale, BioLite HomeStove USD 60) and the Vietnamese biomass gas stove (about USD 70). It is 3–4x the price of basic Vietnamese improved wood stoves (USD 6–10) and comparable to carbon-subsidised African retail prices (USD 5–25). If the USD 25 includes a fan or power supply, it is a strong cost position; this needs checking against the bill of materials.
- **Fuel flexibility.** No major commercial competitor advertises continuous feeding of loose, unprocessed residues such as rice husk and sawdust with Tier 4–5 performance. Mimi Moto and Inyenyeri depend on pellets; ACE, BioLite, and BURN are batch-fed with wood or charcoal. This is GaSIO's clearest potential technical edge, if the CREEC results were obtained on loose residues rather than pellets.
- **Biochar.** Biochar co-production is shared only with TLUD-type stoves (PowerPellet, GASTOV), which are batch stoves. A continuous char-making stove could support both cookstove credits (Gold Standard/Verra metered or fuel-use methods) and biochar CDR credits (Puro/Isometric). Stacking or double-claiming rules would need checking.
- **Scale gap.** GaSIO's documented deployment is a few hundred households (Thanh Hoa, Thai Nguyen, Cu Khoi) plus BEST-project agri-processing units, against 68k (Mimi Moto), tens to hundreds of thousands (ACE), and 5.2M (BURN). Competitors also hold carbon registrations, CCP labels, PAYGo infrastructure, and international brands.

### Gaps
- Envirofit (HM5000, etc.) current tiers and pricing: not found in this session.
- Philips/HPS fan stove current status, the Champion TLUD, Servals, Mwoto, Peko Pe, Lucia/WorldStove, and Elsa: no current 2025–2026 data found in this round.
- Cambodia, Laos, and Indonesia rice-husk gasifier makers: not researched in depth (no results surfaced).
- SINCO (Vietnam) gasifier stove: no results found. Its existence and specs are unverified.
- ACE 2 specs and price, and BioLite HomeStove ISO results: not found.
- Current Mimi Moto household pellet prices and Gold Standard project IDs: not found.

## 4. Camping, military, and emergency segment (GaSIO 3 kW battery-fan field stove)

### Takeaway
The Western camping wood-stove market has two tiers: fanless double-wall "gasifier" cans (Solo Stove, about USD 56–100) and battery or thermoelectric fan stoves (BioLite CampStove 2+, about USD 150). GaSIO's camping stove would compete with BioLite on the fan concept. Its claimed "unlimited continuous cooking" via continuous feed and its 3 kW output are differentiators, but it has no outdoor-retail brand, distribution, or certifications.

### Cited Findings
- BioLite CampStove 2+: retail about USD 149.95 (historic USD 99.93–149.99); boils 1 L in 4.5 min; 2.06 lb (935 g); 3,200 mAh battery; the thermoelectric generator charges the fan and USB devices. Australian retail about AUD 198 (August 2026) — [Trailspace](https://trailspace.com/gear/biolite/campstove-2+); [BuyWisely AU](https://buywisely.com.au/product/biolite-campstove-2); [ShopSavvy review](https://shopsavvy.com/reviews-tldr/biolite-campstove-2+)
- Solo Stove Lite was USD 55.99 on sale (list USD 69.99) and Solo Stove Titan USD 79.99 on sale (list USD 99.99) in December 2025. Both are fanless, natural-draft double-wall stoves. A user comparison notes BioLite costs about USD 130 more than the Solo Lite; the Solo is "light, super-compact, foolproof, unbreakable" but slow to boil — [Bob Vila Dec 2025](https://www.bobvila.com/reviews/solo-stove-deals-last-minute-holiday-shopping-dec-2025/); [Drop forum](https://drop.com/buy/biolite-campstove-bundle/talk)
- BioLite FirePit+ (Bluetooth, rechargeable fan, wood/charcoal) is listed at USD 599.95 at Campmor; another source gives about USD 300 — [Campmor](https://www.campmor.com/collections/stoves-1); [AARP](https://www.aarp.org/money/personal-finance/best-new-firepits/)
- The "Mimi Moto" name is also sold in the US as the "Smokehouse Mimi Moto" smokeless wood camping stove on Amazon, a fan-gasifier crossover into recreation — [Amazon listing](https://www.amazon.com/Smokehouse-Products-Mimi-Moto-Stove/dp/B07BYM9SQL)

### Inferences
- A GaSIO 3 kW battery-fan stove boiling 1 L in about 2 min would be about twice as fast as the BioLite CampStove 2+ (4.5 min). That is a meaningful spec edge if verified. Weight is not stated in the CCS materials and matters a lot in this segment.
- For military and disaster use, the relevant comparators are BioLite, Solo, and generic Chinese fan wood stoves, plus fuel-tab and gas stoves (not researched here). Procurement would probably require MIL-STD or NATO testing, which CCS does not appear to have.

### Gaps
- Chinese generic battery-fan wood gasifier camping stoves (Amazon/AliExpress, about USD 20–50): not researched.
- Military or humanitarian procurement specs for biomass field stoves (UNHCR, NATO): not researched.

## 5. Where competitors are stronger, and where GaSIO may be differentiated

### Takeaway
Competitors are clearly stronger on scale, verified carbon-credit revenue, financing (PAYGo, fuel subscription), brand, and public certification data. GaSIO's possible edge is narrow but real: continuous feed of loose, unprocessed residues, a biochar co-product, a low USD 25 price, local manufacture, and heating. All of this depends on third-party confirmation of the CREEC results on residue fuels and a clear explanation of the 83.7% efficiency figure.

### Cited Findings
- Competitor scale and finance: BURN has sold 5.2M units and is pursuing CCP-labelled credits — [BURN](https://burnstoves.com/media/newsroom/newsroom-1); Mimi Moto has sold 68k units and uses metered credits from fuel sales data — [CCA profile](https://cleancooking.org/?p=11063); ACE uses PAYGo instalments and usage-data-backed credits — [SWITCH-Asia](https://switch-asia.eu/site/assets/files/4046/ace.pdf); BioLite uses Gold Standard credit subsidies — [REI](https://www.rei.com/blog/camp/good-gear-biolite-fuels-outdoor-adventures-and-off-grid-households)
- Carbon-claim context: GaSIO claims 3–5 tCO2 per stove per year. Comparable claims are Mimi Moto 4–5 t — [CCA](https://cleancooking.org/?p=11063); ACE 2–3 t — [Nature Network](https://www.the-nature-network.com/en/?p=1174); and a TLUD/gasifier planning range of 2.5–3.5 t — [Carbon Workbench](https://thecarbonworkbench.com/cookstove-calculator). RMI flags over-crediting and monitoring concerns in cookstove credits — [RMI](https://rmi.org/resources/technical-explainer-clean-and-improved-cookstove-carbon-credits/)
- Barrier in Vietnam: MOIT says biomass gasification models exist but lack adoption because none suit local finances — [MOIT (via search extract)](https://moit.gov.vn/bao-ve-moi-truong/giai-phap-nang-luong-ben-vung-cho-che-bien-nong-san-va-quan-.html)
- Prior art: continuous-flow rice-husk gasifiers have existed since at least around 2010 in the Philippines (Belonio) — [bioenergylists](https://stoves.bioenergylists.org/node/2878); CCS's own continuous-gasifier R&D dates to 2016 — [CCS](http://www.ccspin.org/index.php/en/news-information/303-update-on-continuous-gasifier-r-d-progress)

### Inferences
- **Competitor advantages over GaSIO:**
  1. Scale and manufacturing (BURN, ACE, Mimi Moto).
  2. Registered carbon projects (Gold Standard, Verra, CCP labels) and metered monitoring.
  3. PAYGo or fuel-subscription financing and IoT usage data.
  4. Public, catalog-listed ISO data and peer-reviewed field studies (Mimi Moto).
  5. Global outdoor brand and retail distribution (BioLite, Solo).
- **GaSIO's potential differentiation:**
  1. Continuous feed, which removes batch interruptions and may reduce refuelling emission spikes.
  2. It burns loose residues (husk, sawdust, cobs) without pelletising, which removes the pellet supply chain that limits Mimi Moto and Inyenyeri.
  3. A biochar co-product with possible CDR revenue stacking.
  4. The USD 25 unsubsidised price.
  5. Space heating, useful in northern Vietnam's mountain provinces.
  6. Local repairability.
- The 83.7% efficiency claim is the weakest point. If it is char-credited, presenting it as a headline could undermine credibility with Clean Cooking Alliance, carbon, and investor audiences. Tier 5 (≥50%) without char credit, if true, is already best-in-class.
- Continuous-flow rice-husk gasification is not new in itself (Belonio, Philippines). Any "technology edge" claim should therefore rest on demonstrated tier performance on loose residues at household scale, which the historical continuous-flow household stoves (about 21% efficiency) did not achieve, not on novelty of the concept.

### Gaps
- No independent field (in-home) emissions or usage data for GaSIO.
- No information on whether GaSIO's fan needs mains electricity or a battery, which affects the USD 25 comparison with ACE's solar-battery stove.
- No GaSIO carbon project registration was found in Gold Standard or Verra searches (not directly searched due to tool limits).
