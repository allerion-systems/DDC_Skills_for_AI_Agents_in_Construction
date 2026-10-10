# Evolve Brief — 2026-10-10

Automated scheduled run. Facts come from web searches (sources at bottom); items marked **CONCEPT** are unvalidated design ideas, not engineering claims.

## 1. Fluorspar (CaF2) and fusion

**Uses today:** >50% of fluorspar goes to hydrofluoric acid (HF), the gateway to nearly all fluorine chemistry (refrigerants, fluoropolymers, uranium hexafluoride for the fuel cycle, LiPF6 battery electrolyte). Next come aluminum smelting (cryolite/AlF3) and steel flux. China produces over half of world supply; Mexico, Mongolia and South Africa follow.

**Fusion link:** Fluorspar -> HF -> LiF and BeF2 -> **FLiBe** (2LiF·BeF2) molten salt. FLiBe is a leading liquid-blanket candidate: lithium breeds tritium, beryllium multiplies neutrons (raising tritium breeding ratio above 1), and the salt carries heat and shields structures. July 2026: Kyoto Fusioneering and NGK announced a partnership to commercialize FLiBe and circulation systems. MIT's BABY experiment tests tritium breeding with a surrogate salt (LiF-LiCl).

**Other fusion-adjacent fluorine uses (from general knowledge, verify before citing):** WF6 for chemical-vapor-deposited tungsten plasma-facing coatings; fluoride salts for tritium extraction; fluoropolymer seals/insulation.

**Bottlenecks to watch:** beryllium supply and toxicity, Li-6 enrichment, TF corrosion/redox control in the salt, and Chinese concentration of fluorspar. Fluorspar is rarely the binding constraint; processing capacity for high-purity LiF/BeF2 is.

**Allerion angle:** the property-center mineral work (Hardin County, IL fluorspar district is historic) makes a "fusion-grade fluoride supply chain" a natural thesis. Keep Hicks Dome data labeled ADJACENT per Digital Twin rules.

## 2. Solar roofing (CONCEPT)

State of art: flexible perovskite roof tile (TNO, up to 13.8% module, 12.4% on a curved tile; roll-to-roll capable); Gain Solar showed perovskite and back-contact tiles at Intersolar Europe 2026. Durability data is still thin.

**Concept "SolarSeam":** a roll-formed standing-seam steel roof where the pan is the substrate. Perovskite-on-steel foil laminated at the factory, glass-free fluoropolymer (ETFE) front sheet, seam clips double as busbar connectors so installation is a roofer's job, not an electrician's. Wins: no penetrations, low weight, roofer-installable, warranty split into weatherproofing vs. power. Risks: perovskite lifetime, heat from dark metal, fire code listing.

## 3. Battery build method (CONCEPT)

State of art: Tesla reports dry-process anodes and cathodes on 4680 cells (Feb 2026); solvent drying is a large share of cell cost; sodium-ion dry-processing work published Dec 2025.

**Concept "Brick-Cell":** a structural, sodium-ion, dry-electrode cell sized as a masonry/CMU-compatible block for stationary storage. Cells are the wall; the module housing disappears. Targets cheap, non-flammable edge storage for the data-center pods below. Risks: thermal runaway containment in a load path, code acceptance, lower energy density (irrelevant for stationary).

## 4. Zero-emission modular edge data center canvas (CONCEPT)

Reference: EdgeCloudLink 1 MW off-grid hydrogen modules (company claims); EODev/Leadership Datacenter 110 kVA fuel-cell edge unit.

**Canvas blocks:** (1) Power: rooftop SolarSeam + Brick-Cell storage + electrolyzer/fuel-cell for multi-day gaps. (2) Cooling: direct-to-chip liquid loop, fuel-cell water recycled, heat sold to adjacent buildings or greenhouses. (3) Network: dual-path (fiber + fixed wireless/LEO), BGP anycast to neighbors, WireGuard mesh between pods. (4) Shell: 40 ft shipping-container or 3D-printed form, sited at cell towers, farms, mines. (5) Controls: microgrid EMS that schedules AI inference to solar surplus. (6) Compliance tie-in: FedRAMP-OllaLab-Lean for local inference.

## 5. Next actions
- Decide which concept to prototype first (suggest SolarSeam spec sheet).
- Pull USGS Mineral Commodity Summaries for fluorspar/beryllium numbers.
- Run a deeper search on structural batteries and Li-6 enrichment (not covered this run).

## Sources
- https://www.neimagazine.com/news/japan-partners-target-fusion-salt-supply/
- https://arxiv.org/html/2412.02721v1
- https://www.earthmagazine.org/article/mineral-resource-month-fluorspar-1/
- https://materialdistrict.com/article/perovskite-solar-roof-tile-integrates-renewable-energy-into-architecture/
- https://taiyangnews.info/technology/gain-solar-showcases-bipv-portfolio-with-roof-tile-pv-glass-solutions
- https://www.datacenterdynamics.com/en/news/ecl-announces-3d-printed-hydrogen-powered-off-grid-data-centers
- https://www.powderbulksolids.com/chemical/sustainable-battery-manufacturing-the-dry-process-advantage
- https://www.iws.fraunhofer.de/en/technologyfields/battery-technology.html
