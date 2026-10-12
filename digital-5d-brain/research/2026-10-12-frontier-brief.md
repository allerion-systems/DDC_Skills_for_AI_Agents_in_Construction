# Frontier Brief — 2026-10-12

Automated scheduled run. Status labels: **[Sourced]** from a web search this run, **[Known]** general background not re-verified, **[Concept]** original idea, unvalidated, not engineering advice.

## 0. Second-brain update
- New `research/` lane added to the Digital 5D Brain. One dated brief per run; ideas that survive go to `products/` or a project case study.
- Cross-link: Allerion Digital Twin sits in Hardin County, IL, inside the Illinois–Kentucky fluorspar district [Known]. Section 4 turns this into a product narrative. Keep the Digital Twin rule: Hicks Dome is ADJACENT, not on-property.
- Open loop: this run could not read other Claude sessions' activity (no shared log in this environment). Point the routine at a session-log export to make the "learn from all activity" step real.

## 1. Modular zero-emission edge data center — conceptual canvas
**State of the art** [Sourced]: EdgeCloudLink has shipped a hydrogen-powered modular data center, with zero-carbon claims that are vendor-only. LiquidStack sells prefab immersion-cooled 250 kW–1.5 MW modules. Grid lead times and bring-your-own-power rules push operators to on-site generation. Adoption percentages for liquid cooling vary widely by source, so don't quote them.

**Canvas (one 40-ft container-class module, "EdgePod")** [Concept]
| Block | Choice | Why |
|---|---|---|
| Power | Rooftop/adjacent PV + LFP or sodium-ion battery + H2 fuel cell backup | no combustion on site |
| Compute | 100–500 kW, direct-to-chip liquid | density, heat capture |
| Heat | 50–60 °C return loop sold to greenhouse, district loop, or absorption chiller | turns waste into revenue |
| Water | Closed loop, dry coolers, zero evaporation | siting in dry regions |
| Network | Dual-homed fiber, BGP anycast, WireGuard mesh between pods, out-of-band LTE/Starlink | no single carrier |
| Control | Digital twin of power/thermal; workload shifting to follow solar | cuts battery size |
| Build | Factory-built, crane-set in a day, estimated and tracked in the 5D model (cost + schedule) | ties to the construction stack |
Key unknowns: economics of H2 backup vs longer batteries; heat offtake near the site; permitting. Next step: a 1-page sizing spreadsheet (kW, kWh, m² PV) for a 250 kW pod.

**Networking/coding learning track** (to "become an expert"): L2/L3 fundamentals → BGP/OSPF → EVPN-VXLAN → WireGuard/overlay → eBPF observability → Go or Rust for network tooling. One lab per week; log results in this folder.

## 2. Solar roofing material — "SolarShingle S1" [Concept]
**Baseline** [Sourced]: Oxford PV/Fraunhofer ISE hit 25.6% on a shingled perovskite-silicon tandem module (June 2026 prototype). TNO/ASAT showed a curved composite roof tile with a flexible perovskite module at 12.4% after installation. Reliability and lifetime are the open problems.

**Idea:**
- Interlocking tile with a standard roofing nailing flange and overlap, so roofers install it like a shingle and the overlap is the water barrier. Wiring runs through a hidden channel under the overlap.
- Shingled silicon cells (proven format) with a perovskite top cell later as a drop-in upgrade, so the product ships on silicon and upgrades without a re-roof.
- Front surface: textured fluoropolymer (ETFE-type) or thin glass with a fluorinated hydrophobic coat for self-cleaning. Glass-ceramic option for hail rating and a slate look.
- Under-tile airflow lets the roof preheat ventilation air or a heat-pump source (PVT hybrid).
- Each tile carries a QR/ID, feeding the project's 5D model and warranty record.
Risks: wiring/fire code (rapid shutdown, NEC), hail, thermal cycling, cost per m² against shingles plus panels. Next step: BOM and cost per m² against asphalt shingle plus rack-mounted PV.

## 3. New way of building batteries [Concept]
**"Brick" battery architecture** (design for assembly and disassembly):
1. Dry-electrode, solvent-free coating (fewer process steps, no NMP).
2. Cells made in a rigid, stackable prismatic "brick" with the bus bars on two faces and a reversible mechanical joint (no adhesive), so a bad cell is swapped and the rest recycled.
3. Sodium-ion or LFP chemistry for stationary use; no cobalt or nickel.
4. Bricks double as thermal mass and a structural block in a slab or retaining wall (stationary storage in a building's own structure).
5. Each brick carries an ID and a cycle-history record that goes in the 5D asset model.
Why it matters: the cost is dominated by manufacturing, packaging and end-of-life, not chemistry. Risks: sealing a reversible joint against moisture, and safety certification of a structural battery. Next step: pick one failure mode (joint leakage) and design a test.

## 4. Fluorspar (CaF2): uses and fusion relevance
**Main uses** [Known]: hydrofluoric acid and all downstream fluorochemicals (refrigerants, PTFE and other fluoropolymers, PVDF battery binders, LiPF6 electrolyte, pharmaceuticals); steel and iron flux; aluminum smelting (cryolite/AlF3); uranium hexafluoride for enrichment; glass, enamel, cement; optical-grade CaF2 for UV lenses and lithography.

**Fusion link** [Sourced + Known]:
- FLiBe (LiF + BeF2) molten salt is a leading liquid-blanket candidate. In ARC-class designs it serves as breeder, neutron shield and coolant, and beryllium multiplies neutrons for tritium breeding. The MIT LIBRA experiment studies tritium breeding in FLiBe. Tritium self-sufficiency has never been shown at scale. Beryllium toxicity is a major drawback; LiCl-LiF is a proposed alternative [Sourced].
- Fluorspar is the fluorine source: fluorspar → HF → LiF and BeF2. So any fluoride-salt blanket or molten-salt fission-fusion hybrid is a fluorspar demand driver [Known]. Enriched Li-6 is the harder bottleneck.
- Fluorine under neutron irradiation produces short-lived N-16, a hard-gamma emitter, a shielding and activation issue for fluoride coolants [Known; verify before relying on it].
- Fluorine-based plasma-facing/tritium-handling chemistry (HF/F2 for tritium recovery) is plausible but I have not verified it.
**Allerion angle:** a "fusion-grade fluoride supply chain" narrative for the Hardin County property: fluorspar as a critical mineral feeding batteries (PVDF, LiPF6), solar (fluoropolymer encapsulants), and fusion salts. Needs a deliberate claims review against the Digital Twin rules (REE/inferred vs measured).

## 5. Sources
- https://arxiv.org/pdf/1409.3540 (ARC)
- https://arxiv.org/html/2412.02721v1 (BABY tritium experiment)
- https://pv-magazine-usa.com/2026/06/18/oxford-pv-achieves-25-6-efficiency-for-perovskite-silicon-tandem-module-based-on-shingled-design/
- https://bits-chips.com/article/tno-puts-perovskites-on-rooftops-with-solar-tiles/
- https://www.datacenterdynamics.com/en/news/edgecloudlink-delivers-first-hydrogen-powered-modular-data-center/
- https://reimagine.edgeir.com/liquidstack-unveils-new-turnkey-data-center-solutions-bringing-liquid-cooling-to-the-edge-20230927

## 6. Next-run queue
1. 250 kW EdgePod sizing sheet. 2. SolarShingle BOM vs asphalt+PV. 3. Verify N-16 / fluorine activation and tritium-recovery chemistry with primary sources. 4. First networking lab.
