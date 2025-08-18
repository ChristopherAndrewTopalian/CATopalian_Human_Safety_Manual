# Electric Vehicle Battery Roof Placement - B

**Thermal Management Design Guide — Roof‑Mounted EV Battery Module**

> Focus: thermal control strategies, design targets, and operational rules for a roof‑mounted traction battery module (roof pack). This document assumes the roof pack architecture and ejection concept from the parent README (`Electric Vehicle Battery Roof Placement`).

---

## Executive summary

Roof‑mounting a traction battery brings major safety and serviceability benefits but introduces **higher solar/ambient thermal loading**. With integrated thermal design — reflective skins, insulation, active cooling, and BMS policies — the pack can remain inside safe operating temperatures even in extreme climates. This doc lists practical, testable measures, materials, and operational rules to achieve that.

---

## Design targets (numeric)

* **Cell core operational range (nominal)**: **0°C – 45°C** (charging derated above 45°C)
* **Short‑term spike tolerance**: cell case < **60°C** for up to 30 minutes
* **Surface skin max**: outer roof skin may reach **≤ 95°C (203°F)** in extreme sun; design should prevent core > 60°C
* **Passive cooling delta target**: insulated pack core should limit ΔT (skin→core) ≤ **25°C** under 1 kW/m² solar load
* **Time to ejection readiness**: pack must meet 'safe ejection' conditions (HV contactors open, coolant sealed) within **10 seconds** of command

---

## Thermal management strategy – layered approach

1. **Solar rejection (outermost)**

   * Use high‑reflectivity paints/films (total solar reflectance, TSR ≥ 0.65) or spectrally selective coatings that reflect near‑IR while maintaining reasonable emissivity for nighttime cooling.
   * Consider lightweight passive shade (deployable micro‑awning) for parked vehicles.

2. **Outer shell & air gap (double‑skin)**

   * Construct a ventilated double skin: outer skin + **20–40 mm** air gap to reduce conductive heat transfer; rear exhaust vents create chimney effect.

3. **Insulation layer**

   * Use aerogel blankets (thermal conductivity k ≈ 0.013–0.020 W/m·K) or vacuum insulated panels (VIPs) where weight allows. Target total R‑value ≥ **R2** (imperial) for the roof cassette.

4. **Thermal sink / PCM**

   * Integrate Phase Change Materials (PCMs) tuned to **45–55°C** that absorb mid‑day heat spikes. Ensure PCM containment and long‑life cycles (10k cycles target).

5. **Active liquid cooling plate**

   * Thin cold plate integrated into the module lid: ethylene‑glycol/water mix, dry‑break quick‑disconnect for emergency ejection.
   * Coupled to vehicle HVAC chiller loop for pre‑cooling when parked or during high loads.

6. **BMS policy & thermal controls**

   * BMS monitors pack skin temp sensors and several internal cell thermistors. Charge rate is derated above **45°C** and disabled above **55°C**.
   * Pre‑conditioning: on approach/park near a charger, vehicle pre‑cools pack to <40°C if ambient >30°C.

7. **Vent & off‑gas management**

   * Off‑gas chimneys point upward away from cabin with rupture panels that open at controlled overpressure. Include catalytic scrubber or gas‑capture port for first responders.

---

## Materials & components (recommended)

* **Outer skin**: aluminum or carbon fiber panel with solar‑reflective coating (ceramic‑based paints recommended)
* **Insulation**: silica aerogel blanket or VIP (use VIP around perimeter, aerogel for conformal coverage)
* **PCM**: commercial paraffin or salt hydrate PCM with encapsulation in aluminum trays
* **Coolant plumbing**: stainless steel/fused polymer dry‑break couplers rated for repeated emergency disconnects
* **Sensors**: 4–8 NTC thermistors distributed across module (cells, pack center, inlet/outlet)
* **Electronics**: redundant BMS with thermal safety watchdogs; thermal fuse cartridges

---

## Operational rules & BMS sequences

1. **Normal operation**: maintain target cell core 15–35°C for optimal life
2. **Hot ambient response**:

   * If surface skin > 65°C, increase coolant flow and close vents to force liquid cooling predominance.
   * If core > 45°C: reduce charge/discharge power to 50%.
   * If core > 55°C: disable HV outputs and require service intervention before re‑use.
3. **Ejection pre‑checks** (sequence before roof release): HV contactors open → HV pre‑charge path cleared → dry‑break connectors sealed → confirmation LEDs → mechanical release permitted.

---

## Testing & validation

* **Solar soak test**: 1000 W/m² solar simulator on full roof cassette for 2 hours; measure core temp delta and ensure core < 60°C
* **Salt‑fog corrosion**: 1000‑hour ASTM B117 salt‑fog exposure on exterior + connector corrosion tests
* **Drop & ejection test**: 1000 ejection cycles at ambient 20–50°C and at high temp 60–80°C; validate dry‑break integrity
* **Thermal runaway containment**: induce cell thermal runaway in test cell inside module; confirm off‑gas venting and suppression engages, and outer skin temps remain ≤ 120°C at 1 m distance

---

## Park & user‑experience features

* **Auto‑shade mode** when parked in high sun: deploy reflective micro‑shade to reduce roof skin by \~20–40%
* **Remote pre‑cooling**: allow user to pre‑cool roof pack before charging via app
* **Status indicators** on access panel: green=ready, amber=pre‑cooling, red=unsafe/no eject

---

## Emergency responder procedure (brief)

1. Confirm scene safety; approach vehicle from leeward side.
2. Use responder key to open access panel and read status LEDs.
3. If safe to eject (LEDs indicate HV isolated), press guarded eject button or follow authenticated wireless command.
4. Bag the ejected pack with the containment sack, seal, and move to safe area per hazmat SOP.

---

## Notes & caveats

* The roof pack thermal strategy increases complexity and weight; margin engineering, chassis tuning, and safety analysis are required for each platform.
* Hail and puncture resistance must be validated (see future doc `Electric_Vehicle_Battery_Roof_Placement_C` for hail & impact design).

---

## References & further reading

* EV thermal management textbooks and SAE papers (search terms: "EV battery thermal management", "solar load on vehicle roof", "battery cooling preconditioning")
* ASTM B117 Salt Fog for corrosion testing
* UL 9540A for thermal runaway testing

---

## TODO / next steps

* Generate a one‑page responder quick card (diagram + eject steps)
* Create a lightweight spec for the dry‑break connectors and responder access panel
* Simulate solar soak on target vehicle shapes

---

//----//

// Dedicated to God the Father  
// All Rights Reserved Christopher Andrew Topalian Copyright 2000-2025  
// https://github.com/ChristopherTopalian  
// https://github.com/ChristopherAndrewTopalian  
// https://sites.google.com/view/CollegeOfScripting

