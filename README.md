# SolidWorks Simulation Portfolio

Showcase of core FEA skills using **SolidWorks Simulation** across static, modal (frequency), and thermal analyses. Each study includes CAD, setup notes, mesh details, boundary conditions, solver settings, and result snapshots.

> **Goal:** Demonstrate practical analysis workflow—problem definition → assumptions → model prep → meshing → loads/BCs → solver → verification 

---
# Animation
![Stress Animation gif](https://github.com/user-attachments/assets/8eabe372-6f06-4f32-8f23-7b7b0ce7bd48)



## Repository Structure
```
Connector Bracket/                 # Static stress analysis of a bracket under service loads
Frequency Analysis Crankshaft/     # Modal analysis of a simplified crankshaft
Frequency Analysis Shaft/          # Modal analysis of a stepped shaft
Static Analysis Cantilever Beam/   # Benchmark static deflection & stress of a cantilever
Thermal Analysis Heat Sink/        # Steady-state thermal analysis & temperature field
LICENSE
```
Each folder contains:
- `CAD/` or `*.SLDPRT`, `*.SLDASM` – geometry.
- `Simulation/` – study files (`*.SLDPRT/ASM` with studies).

---

## Featured Studies

### 1) Connector Bracket — Static Stress
- **Objective:** Check maximum von Mises stress and safety factor under bolt/fixture loads.
- **Setup:** Fixed face at mounting holes, bolt preload or equivalent forces; material: mild steel (e.g., AISI 1020).
- **Mesh:** Curvature‑based; local refinement at fillets/holes.
- **Results:** Peak stress at hole fillets; deflection within serviceable limits; SF reported against yield.

### 2) Crankshaft — Modal (Frequency) Analysis
- **Objective:** Identify natural frequencies and mode shapes to avoid resonance.
- **Setup:** Bearing supports as remote restraints; free–free or supported cases compared.
- **Results:** First few bending/torsional modes listed; recommendations on speed ranges.

### 3) Stepped Shaft — Modal (Frequency) Analysis
- **Objective:** Baseline modal behavior of a shaft with diameter transitions.
- **Setup:** Ends as simply supported; material: steel.
- **Results:** First 6 natural frequencies & mode shapes with percent differences vs. hand calcs (if applicable).

### 4) Cantilever Beam — Static Verification
- **Objective:** Validate FEA vs. classic beam theory.
- **Setup:** Fixed end constraint; tip load.
- **Results:** Deflection and stress agree with theory within acceptable error (mesh convergence shown).

### 5) Heat Sink — Steady‑State Thermal
- **Objective:** Temperature distribution for a heat source with convective cooling.
- **Setup:** Heat generation/heat flux on base; convection on fins; material: aluminum.
- **Results:** Max temperature and thermal gradient; sensitivity to convection coefficient.


---

## Analysis Workflow (Common to All)
1. **Problem Definition:** Requirements, load cases, success criteria.
2. **Geometry Prep:** Simplify small features; ensure contacts and interfaces are clean.
3. **Material Selection:** Elastic properties (E, ν), density, thermal conductivity where relevant.
4. **Contacts & Fixtures:** Appropriate restraints (fixed, remote, bearing) and contact types (bonded, no‑penetration as required).
5. **Loads:** Forces, pressures, bolt preloads, heat flux/power, convection.
6. **Meshing:** Curvature‑based mesh; local refinements; **mesh convergence** check on stress/deflection/temp.
7. **Post‑Processing:** Von Mises, displacement, factor of safety, natural frequencies/modes, temperature fields.
8. **Validation:** Compare with hand calcs or literature where possible.
9. **Reporting:** Summarize assumptions, limitations, and recommendations.

---

## How to Open
- Requires **SolidWorks** with **Simulation** add‑in (version 2021 or later recommended).
- Open the part/assembly, then go to **Simulation** tab → **Study** to view setup and results.
- If results are not present, right‑click the study → **Run** to solve.


---

## Skills Demonstrated
- Static, thermal, and modal FEA with SolidWorks Simulation  
- Geometry simplification & contact modeling  
- Mesh strategy and convergence checks  
- Hand‑calculation validation and safety‑factor assessment  
- Result interpretation & design recommendations

---

## License
This project is released under the license in the root `LICENSE` file.

## Contact
**A. Zia** — open to roles in CAE/Design/Mechanical Engineering.  
Reach out via GitHub Issues or your preferred channel.
