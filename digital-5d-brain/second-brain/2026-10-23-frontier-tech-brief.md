# Second Brain Entry — Frontier Tech Brief (2026-10-23)

Automated scheduled run. Research items cite sources; **inventions are concept-level hypotheses, not validated designs.** Numbers marked (unverified) came from secondary or promotional sources.

---

## 1. Edge Zero-Emission Modular Data Center — Concept Canvas

**State of the art (found):** EdgeCloudLink (ECL) runs a 1 MW hydrogen fuel-cell modular site in Mountain View, CA — liquid cooling, no diesel, grid/battery backup, claimed PUE 1.05 (company claim, unverified), 3–6 days on-site H2 storage. Partnership with PowerCell on a FlexGrid microgrid. Sources: [DCD](https://datacenterdynamics.com/en/news/edgecloudlink-delivers-first-hydrogen-powered-modular-data-center), [Data Center Frontier](https://www.datacenterfrontier.com/energy/article/55090918/ecl-advances-its-vision-for-hydrogen-powered-data-centers).

**Canvas (ALLERION "Edge Pod" hypothesis):**

| Block | Concept |
|---|---|
| Unit | 40-ft ISO-footprint pod, 250 kW–1 MW IT, factory-built, crane-set on a slab/piers (fits construction-estimating workflow: repeatable SKU, 5D cost model) |
| Power | Solar canopy + on-site battery (see §4) as primary; fuel cell (H2 or biogas) as firming; grid optional. No diesel |
| Cooling | Direct-to-chip liquid + immersion; rejected heat sold/used (greenhouse, building hydronic loop, district heat). Closed loop; fuel-cell water reused |
| Network | Dual-path: fiber + 5G/private LTE + LEO backhaul; local inference, sync to core off-peak |
| Siting | Wastewater plants, hospitals, mines, ag, rural substations, reclaimed industrial sites (heat offtaker nearby is the key siting rule) |
| Control | Carbon-aware workload scheduler: shift deferrable jobs (training, batch) to solar peaks; keep latency-critical inference local |
| Revenue | Compute-as-a-service + heat + demand-response; sold as a leased "pod + site prep" package |
| Risks | H2 logistics/cost, permitting for H2 storage, fuel-cell lifetime, thermal-offtake dependence, noise/zoning |

**Open questions to research next:** SOFC on biogas vs PEM on H2; immersion-fluid PFAS exposure (relevant to §5); microgrid interconnect rules per state.

**Networking/coding expertise log (to keep growing):** edge topology = BGP/EVPN leaf-spine inside pod, WireGuard/IPsec overlay to core, SD-WAN across carriers, k3s/Nomad at edge, GitOps (Flux/Argo) fleet management, OpenTelemetry for power+thermal+compute in one telemetry stream.

---

## 2. Solar Roofing That Is the Roof — Invention Concept

**State of the art (found):** TNO (Apr 2026) built the first perovskite solar roof tile: 12.4% after curving onto the tile, 13.8% flexible module pre-bend; roll-to-roll compatible; spinout Perovion targets foil production by ~2030; lifetime is the hurdle. Source: [TNO](https://www.tno.nl/en/newsroom/2026/04/perovskite-solar-roof-tile/), [TaiyangNews](https://taiyangnews.info/technology/tno-integrates-perovskite-module-in-rooftile-with-124-efficiency). A USPTO filing covers a perovskite shingle with oxygen/moisture protection ([patent](https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/12647063)).

**Concept: "SolarCourse" — a roofing course, not a panel on a roof**
1. **Substrate:** standard-profile architectural shingle/tile body (steel-backed or composite) so installers use normal nailing patterns and flashing details — it must be installed by roofers, not electricians.
2. **Active layer:** perovskite-on-silicon tandem or CIGS/flexible perovskite foil laminated into the exposed zone; the headlap zone carries no cells.
3. **Encapsulation:** glass-free polymer + thin-film barrier with edge seal (the lifetime problem lives here; target accelerated damp-heat + thermal cycling per IEC 61215 before any claim).
4. **Interconnect:** each shingle has built-in plug-in contacts in the overlap; a course self-wires into a string with the nail line sealed above the contact. Bypass diode per shingle for shade tolerance.
5. **Dual function:** cool-roof reflective non-active zones, hail-impact rating target (UL 2218 Class 4), Class A fire rating.
6. **Smart layer:** per-course microinverter/optimizer at the ridge; fault location by string signature.
7. **Estimating hook:** price per square (100 sq ft) installed vs. roof + separate PV; payback is roof-replacement avoided cost + energy.

**Why it could win:** displaces a cost the owner already pays (roof). **Why it may not:** lifetime (20–30 yr roof vs. perovskite stability), repairability, wiring/code (NEC 690 rapid shutdown), fire classification. Needs a prior-art/patent search before any filing.

---



## 4. Battery Build Method — Design Concept

**State of the art (found):** Dry-electrode manufacturing removes solvent coating/drying/recovery. Tesla stated 4680 cathodes and anodes are now dry-made (Feb 2026); a Nature Communications paper (Dec 2025) reports dry-processed sodium-ion cells; LG ES plans an all-solid-state dry-electrode pilot line H2 2026 and sodium-ion samples 2027. Sources: [Emsclad IBS 2026 review](https://www.emsclad.com/international-battery-seminar-2026-recap/), [SMM](https://news.metal.com/newscontent/104036774-solid-state-battery-lg-energy-solution-turned-profitable-in-q2-h2-to-launch-all-solid-state-dry-electrode-pilot-line2), [Nat. Commun.](https://doaj.org/article/213bb1b486b04483a2cc718996e64e5c). Cost-reduction claims (~40–50%) are from vendors (unverified).

**Concept: "Print-Press-Stack" stationary sodium-ion battery for edge pods and buildings**
- **Chemistry:** sodium-ion (hard-carbon anode, layered-oxide or Prussian-white cathode), aluminum current collectors on both sides (no copper) — cheap, no lithium/cobalt/nickel, wide temperature tolerance, safe to ship at 0 V.
- **Process:** fully dry electrode powders → hot-calendered films → continuous lamination; no NMP/water solvent loop.
- **Pack architecture:** cell-to-structure *enclosure* — cells bonded into a structural stationary rack that doubles as the pod's floor/wall frame, removing a layer of racking steel.
- **Modularity:** hot-swappable 5 kWh drawers with per-drawer BMS and a 48 V bus; failed drawers swapped by a technician, not a crane.
- **Lifecycle:** drawers return to a regional refurbisher; Al and hard carbon recycle simply.
- **Targets to test (not claims):** ≥6,000 cycles at 80% DoD, ≥120 Wh/kg cell level, –20 °C to 55 °C operation.
- **Why stationary:** energy density matters less, cost/safety/cycle life matter more, which is where sodium-ion fits.

Gap found: no confirmed source on structural batteries — needs a dedicated search.

---

## 5. Fluorspar (CaF₂) — Uses and Fusion Relevance

**Established uses (found):** acid-grade (>97% CaF₂) reacted with sulfuric acid → hydrogen fluoride (HF) → the entry point to most fluorochemicals; aluminum fluoride/synthetic cryolite for aluminum smelting; metallurgical-grade flux in steel and foundries; HF used in Li-ion electrolytes (Benchmark projects Li-ion fluorspar demand >1.6 Mt by 2030; the specific LiPF₆ route was not confirmed in the source). U.S. imports essentially all of its supply; designated a critical mineral in 2018. Sources: [Benchmark](https://source.benchmarkminerals.com/article/fluorspar-the-quiet-achiever-of-the-lithium-ion-battery-boom), [EARTH Magazine](https://www.earthmagazine.org/article/mineral-resource-month-fluorspar-1/), [Oregon Group](https://theoregongroup.com/commodities/fluorspar/) (promotional — treat with caution).

Other well-known downstream uses (general knowledge, not re-verified this run): refrigerants and fluoropolymers (PTFE), uranium enrichment via UF₆, glass/ceramics/enamel, optical CaF₂ lenses and windows (UV/IR transparent), fluoride toothpaste/water (via HF-derived fluorides), pharma and agrochemical fluorinated molecules.

**Fusion link (found):**
- FLiBe (LiF + BeF₂) is a leading liquid-blanket candidate: lithium breeds tritium, beryllium multiplies neutrons, the salt carries heat and shields. MIT's BABY experiment tests FLiBe breeding at ~100 mL; Kyoto Fusioneering and NGK are working to commercialize FLiBe. Sources: [BABY](https://arxiv.org/abs/2412.02721), [ARC](https://arxiv.org/pdf/1409.3540), [NEI](https://www.neimagazine.com/?p=106113).
- Fluorspar is the *upstream fluorine source*: CaF₂ → HF → LiF/BeF₂. Fusion blanket volumes could create a small but strategic high-purity fluoride demand; beryllium supply and toxicity are the harder constraints than fluorine.
- Open technical problems: tritium extraction from salt; redox control, because tritium forms corrosive TF; salt purity specs; beryllium handling.
- Hybrid fusion–fission concepts that dissolve fertile/fissile fluorides (ThF₄/UF₄) in the salt appear in the literature; one cited APEX study was retracted, so don't rely on its numbers. Source: [Energies 2024](https://doaj.org/article/03c4398bbebb4c1ba66a7e6ad1456675).

**ALLERION tie-in:** the Allerion Digital Twin covers a Hardin County, IL fluorspar/REE property. Fusion-grade fluoride demand is a long-horizon narrative angle; keep the repo's rule — Hicks Dome data is ADJACENT, not on-property, and REE claims below 310 ft are inferred. Do not present fusion demand as a near-term offtake.

**Next research:** high-purity CaF₂→LiF/BeF₂ conversion routes and cost; U.S. fluorspar supply (Illinois–Kentucky district); isotopically enriched Li-6 requirement for FLiBe (a bigger bottleneck than fluorine).

---

## Backlog for the next scheduled run
1. Structural battery search; CATL sodium-ion EV status from primary source.
2. Patent landscape check for roofing-integrated PV (before any "invention" claim).
3. Edge pod: PUE/thermal model spreadsheet and a 5D cost sheet per pod.
4. Fusion fluoride supply chain figures (Li-6, BeF₂, high-purity LiF).
5. Sweep other repos' recent Claude activity for second-brain updates (not done this run; only this repo's brain was located).
