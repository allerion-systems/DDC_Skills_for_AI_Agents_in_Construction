# Fluorspar (CaF2): all major uses, and its role in nuclear fusion

*Research note, 2026-10-11. Confidence tags: [S] sourced this run, [K] general technical knowledge, verify before relying on it.*

## 1. What it is
Fluorspar = fluorite = calcium fluoride (CaF2). It is the main ore source of fluorine. Grades: **acid-grade** (>97% CaF2, feeds HF), **metallurgical-grade** (60-85%, steel flux), **ceramic/optical-grade**. Listed on the 2025 USGS Critical Minerals List; the US imports essentially all of it [S: metaltechnews 2026-08, ASX filings; company claims, directional]. Supply news: Canada Fluorspar restarting St. Lawrence (target ~200 kt/y), Ares Strategic Mining Lost Sheep (Utah), Orbia (Mexico, integrated mine-to-fluorochemicals) [S].

## 2. Uses (value chain)
Most acid-grade spar goes: CaF2 + H2SO4 -> **HF**. HF is the gateway to nearly everything.

| Branch | Use | Notes |
|---|---|---|
| Metallurgical | Steel/ferroalloy slag flux, foundry, welding-rod coatings | Lowers slag viscosity/melting point [K] |
| Aluminum | AlF3 and cryolite for Hall-Heroult bath | Big HF consumer [S] |
| Fluorocarbons | Refrigerants (HFCs, HFOs), blowing agents | HFC phase-down shifting demand to HFOs [K] |
| Fluoropolymers | PTFE, PVDF, FEP, ion-exchange membranes (PEM electrolyzers/fuel cells) | PVDF = Li-ion cathode binder [K] |
| Batteries | LiPF6 electrolyte salt, LiFSI/LiTFSI, fluorinated additives (FEC) | Direct tie to storage buildout [S] |
| Nuclear fuel cycle | HF -> UF4 -> **UF6** for enrichment | Every enriched-uranium reactor depends on it [K] |
| Semiconductors / electronics | HF etch, NF3 and other fluorinated chamber-clean gases, photoresist chemistry | [K] |
| Optics | Single-crystal CaF2 lenses/windows (UV to IR, 193 nm lithography) | Needs optical-grade spar or synthetic [K] |
| Pharma/agro | ~20-30% of drugs and many agrochemicals contain fluorine | [K] |
| Glass, ceramics, enamel | Opacifier, flux | [K] |
| Cement | Mineralizer lowering clinker burn temperature | [K] |
| Insulation gases | SF6 in switchgear (high GWP, being phased down) | [K] |

## 3. Fusion: where fluorine actually matters
Fluorspar itself is not put in a reactor. It is the upstream feedstock for **fluoride salts and fluoropolymers** that fusion designs use.

1. **FLiBe (Li2BeF4 = 2 LiF + BeF2) liquid breeder/coolant blanket.** Lithium-6 breeds tritium, beryllium multiplies neutrons (n,2n), fluorine-rich salt carries heat and shields. Needed because tritium breeding ratio (TBR) must exceed 1 for self-sufficiency. Scale: an ARC-class plant needs on the order of **250,000 L** of FLiBe; MIT LIBRA targets a ~500 L test; Kyoto Fusioneering + NGK are partnering to commercialise FLiBe and its supply [S: arXiv 2412.02721, Nucl. Fusion 65 026037, NEI Magazine]. Every tonne of FLiBe is a fluorspar -> HF -> LiF/BeF2 chain, so **fusion adds a new demand node for acid-grade spar and a hard dependency on lithium-6 enrichment and beryllium**.
2. **Beryllium-free alternatives:** FLiNaK-type and ClLiF (LiF+LiCl) salts; ClLiF is being used as a surrogate (MIT BABY) and one neutronics study found it competitive on TBR and energy multiplication [S]. Trade-off: less fluorine demand, but chlorine corrosion and activation questions.
3. **Salt chemistry problems the field must solve [K]:** tritium appears as TF (very corrosive) unless the redox potential is held reducing (e.g., Be metal or similar redox control); tritium extraction from salt; corrosion of structural alloys (Cr leaching); low tritium solubility means permeation to coolant loops; F-19 activation (N-16 gamma, ~7 s) affects shielding and maintenance.
4. **Fluoropolymers and seals** in cryogenic, vacuum and tritium-handling systems (PTFE/PVDF gaskets, insulation), with radiation-damage limits [K].
5. **Fuel-cycle fluorine:** UF6 enrichment infrastructure also underpins fission-fusion hybrid concepts and fission baseload that fusion will compete/co-exist with; HF-based processing for lithium and beryllium purification [K].
6. **Plasma processing:** NF3/SF6/CF4 chemistries used in wall conditioning and tritium-retention removal studies (fluorine/oxygen glow discharges) [K, lower confidence].

## 4. Opportunities for Allerion (Hardin County, IL fluorspar district)
- Allerion Digital Twin already sits in the Illinois-Kentucky fluorspar district and the Hicks Dome REE/fluorite system (label Hicks Dome as ADJACENT per project rules).
- Positioning: "domestic acid-grade fluorspar for batteries, nuclear fuel cycle and fusion salts" is a defensible procurement story (USGS critical mineral, DOD/DOE interest).
- Suggested next steps: (a) map byproduct fluorite grade and HF-feedstock spec against acid-grade (97%) thresholds in the twin; (b) track DOE fusion-materials FOAs and FLiBe supply-chain announcements; (c) model downstream value uplift: spar -> HF -> LiPF6/LiF.
- Do not claim on-site tonnage or grade beyond measured data.

## Sources (this run)
- Metal Tech News, "Fluorspar reliance reaches beyond the mine" (2026-08) https://www.metaltechnews.com/story/2026/08/25/critical-minerals-alliances-2026/fluorspar-reliance-reaches-beyond-the-mine/2907.html
- Advancing Tritium Self-Sufficiency in Fusion Power Plants: BABY experiment https://arxiv.org/abs/2412.02721
- Delaporte-Mathurin et al., Nucl. Fusion 65 026037 (2025) https://iris.polito.it/bitstream/11583/2996739/1/Delaporte-Mathurin_2025_Nucl._Fusion_65_026037.pdf
- NEI Magazine, Japan partners target fusion salt supply https://www.neimagazine.com/news/japan-partners-target-fusion-salt-supply/
- MIT PSFC, tritium breeding in molten salt https://www.psfc.mit.edu/research-areas/tritium-breeding-in-molten-salt-kevin-woller/
