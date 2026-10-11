# Invention disclosures (conceptual, unvalidated)

*2026-10-11. These are design concepts, not tested products. Nothing here is a patentability opinion; run a prior-art search before any filing. Numbers are first-order estimates to be checked.*

## A. SunLap: roofing that is the solar panel

**State of the art (so we know what is not new):** Tesla Solar Roof, GAF Energy Timberline Solar, CertainTeed Apollo, SunTegra, metal-seam BIPV. Perovskite-silicon tandem modules are only at pilot scale (Fraunhofer ISE/Oxford PV shingled tandem, 1.92 m2, 491 W, 25.6%, June 2026); no commercial perovskite roof tile confirmed [S: pv-magazine, Fraunhofer ISE]. Real pain points: per-tile wiring, roofer vs electrician split labor, leak risk at penetrations, heat build-up lowering output.

**Concept:** a roofer-installable interlocking tile where the roof deck carries the electrical bus.
1. **Tile:** 2 mm tempered/anti-reflective glass front, shingled heterojunction silicon strips (tandem-ready footprint), polymer/glass-fibre back, Class A fire-rated, hail rated UL 2218 target.
2. **Rail-bus architecture (the novel part):** the tile nails/clips onto a pre-wired **batten rail** (extruded aluminium + insulated copper busbar pair, 600 mm modules). Tiles make dry blade contact with the rail through a sealed, gasketed pin when fastened. No MC4 cables on the roof; roofers lay tile, electrician only terminates the rail ends at the ridge junction.
3. **Ventilated cavity (BIPV/T):** rail height creates a 25-40 mm air channel. Warm air feeds a heat-pump/HRV or DHW loop, cooling the cells (about -0.3 %/K coefficient for Si) and giving a second energy output.
4. **Module-level electronics:** microinverter or DC optimizer per 8-12 tile string at the rail, not per tile, so failed tiles are swapped with a blade-contact release tool.
5. **End-of-life:** reversible butyl/PIB edge seal rather than EVA lamination where possible; glass/silicon separable for recycling.
**Key risks:** rail corrosion/arc-fault safety (NEC 690 rapid shutdown, UL 1703/61730), water ingress at contacts, wind uplift (ASCE 7), cost vs shingles. **Prototype test plan:** 3 m2 mock roof, thermal camera, IV curve at 20-70 C, water-spray and 1000-cycle contact fatigue.

## B. Reassemblable battery: dry, bipolar, debondable

**State of the art:** dry-electrode coating (Tesla/Maxwell lineage; equipment demand surging), sodium-ion at scale (CATL Naxtra; MIT TR 10 Breakthrough Technologies 2026), solid-state pilot lines in China with small-batch production expected ~2027 [S]. Cell-to-pack and structural packs exist.

**Concept ("RePack"): build for disassembly and for stationary edge use.**
1. **Chemistry:** sodium-ion (hard-carbon / layered-oxide or Prussian-white) for stationary sites: no cobalt/nickel/lithium, tolerant of cold and deep discharge, lower fire risk. Optional LFP variant.
2. **Process:** solvent-free dry electrode (PTFE/fibrillised binder; flag PFAS regulatory exposure and test PVDF-free alternatives like cellulose or polyolefin binders), roll-pressed on aluminium (sodium-ion allows Al on both sides, no copper).
3. **Bipolar stack:** a single Al current collector with anode on one face and cathode on the other, sealed in a polymer frame. Removes tabs and most inactive mass; raises voltage per frame. Main risk: sealing and electrolyte ionic crosstalk between frames (needs solid/gel or well-sealed frames).
4. **Debondable structure:** frames bonded with thermally or electrically triggered debonding adhesive and a honeycomb recycled-aluminium shell used as pack structure and cold plate. Result: bad frames can be pulled, remaining frames re-graded for second life.
5. **Pack intelligence:** per-frame sense lines, state-of-health logging to a digital passport (EU Battery Regulation direction).
**Key risks:** bipolar leakage, dendrite/Na plating at the frame edge, debond adhesive aging. **First experiment:** 3-frame coin-to-pouch bipolar pouch with gel electrolyte, 500 cycles, measure interframe leakage current.

## C. Conceptual canvas: modular zero-emission edge data center ("ECO-Pod")

State of the art: EdgeCloudLink hydrogen-fuel-cell modular DCs (PUE ~1.05 claimed, rear-door heat exchangers); WEDISTRICT Luleå fuel-cell + immersion + district-heat demo [S: DCD, SDxCentral, RISE]. Most material is 2023 vintage; no 2026 scale-up evidence found.

| Block | Design |
|---|---|
| Customer / use | Edge inference, 5G/6G MEC, private AI on construction sites, remote mines, utilities |
| Form factor | 40-ft ISO container (or 20-ft), 50-250 kW IT per pod, stackable to 1 MW cluster |
| Power | Solar canopy + sodium-ion BESS (4-8 h) + firm source: PEM fuel cell on green H2 or SOFC on biogas. Grid optional |
| Cooling | Direct-to-chip liquid at 45 C supply, dry coolers, no evaporative water. Optional single-phase immersion for dense GPU nodes |
| Heat reuse | 45-60 C return to greenhouse, aquaculture, DHW or district loop; this is the main zero-emission differentiator |
| Water | Fuel-cell product water recycled to humidifiers and site use |
| Network | Dual diverse uplinks (fiber + LEO/fixed wireless), BGP + EVPN-VXLAN spine-leaf inside, 400G, WireGuard overlay to cloud, k3s/Kubernetes with zone-aware scheduling |
| Control | Digital twin of pod (power, thermal, workload) with carbon- and heat-aware scheduling: move batch jobs to when H2/solar are cheapest |
| Cost drivers | Electrolyzer/H2 storage, fuel cell stack life, GPU capex |
| Risks | Hydrogen safety (ATEX/NFPA 2), green H2 cost, permitting, uptime SLA |

**Back-of-envelope sizing (first-order):** 250 kW IT x PUE 1.1 = 275 kW; 6.6 MWh/day. PEM fuel cell at about 50% LHV efficiency is about 16.7 kWh_e per kg H2, so about 395 kg H2/day. That is heavy logistics, so 50-100 kW pods (about 80-160 kg/day) or solar+battery with grid or biogas backup are the realistic first products. Solar alone cannot carry 24/7 load: at roughly 1 kWh/m2/day of delivered output you would need about 6,600 m2 for 250 kW, so canopy covers only daytime offset.

## D. Networking and coding skill-building plan (expert track)
- Networking: BGP/EVPN-VXLAN, MPLS basics, QoS, RDMA/RoCE for AI clusters, SD-WAN, WireGuard, DNS/anycast, observability (gNMI/OpenTelemetry), Zero Trust. Lab: containerlab + FRRouting spine-leaf.
- Coding: Python/TypeScript/Go; Rust for edge agents; Terraform/Ansible; k3s; Prometheus/Grafana.
- Suggested repo: `allerion-edge-lab` with containerlab topologies plus a thermal/power pod simulator.

## Next steps (priority)
1. Prior-art search on rail-bus roof tile and debondable bipolar sodium-ion frames.
2. Build the pod simulator (power + thermal + heat reuse) in Python.
3. Decide with Joey which invention to pursue: SunLap fits the construction audience best.
