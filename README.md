# Fixed Wing Surveillance Drone
 
Engineering notebook for a tailless endurance flying wing: derivations, design reasoning, and build process, starting with a hand-launched glider and working toward a powered version.
 
 
## Status
 
**Phase 1: hand-launched glider.** Planform closed, airfoil provisionally selected (HS 3.0/8.0B), root and tip hot-wire templates cut. Airfoil validation and first wing in progress.
 
## Design at a glance
 
| Parameter | Value |
|---|---|
| Span | 1.1 m |
| Root / tip chord | 27.5 cm / 16.5 cm |
| Taper ratio | 0.6 |
| Aspect ratio | 5.0 |
| Wing area | 0.242 m² |
| Wing loading | ≈ 5.2 N/m² |
| All-up weight | ≈ 130 g |
| Trim speed | ≈ 3.8 m/s |
| Reynolds number | ≈ 70k root / ≈ 42k tip |
| Airfoil | HS 3.0/8.0B, reflexed, 8% thick (provisional) |
| Construction | Hot-wire-cut XPS foam |
 
## Summary
 
The mission is endurance: stay aloft as long as possible. From the steady-glide equations, aspect ratio sets the aerodynamic ceiling for both glide ratio and endurance, but wing loading only matters for endurance, since sink rate scales as $\sqrt{W/S}$ while it cancels out of glide distance entirely. That makes wing loading the first design point to fix.
 
Following that through fabrication, 3D printing in ABS turned out to lock wing loading in the slicer (plan area cancels) at a heavy weight penalty, which, along with iteration speed and reparability, drove a switch to hot-wire-cut XPS foam.
 
For tailless stability, I use lifting-line theory to connect the spanwise circulation to lift, induced drag, and yaw, and compare elliptic and bell spanloads. A bell load with sweep gives proverse yaw and finless directional stability (the Prandtl-D result), but a two-template hot wire can only cut linear twist. So the first wing is hot-wire-native: a reflexed section, moderate sweep, conservative linear washout, and small winglets, with the bell spanload as a later goal.
 
The planform is closed by choosing the smallest taper ratio whose tip stays above a Reynolds floor of about 40k, giving $\lambda \approx 0.6$ and $AR \approx 5.0$. The notebook also documents which numbers are still placeholders and how the design converges as they're replaced.
 
## Notebook
 
Full derivations and design reasoning: [Fixed_Wing_Surveillance_Drone_Project.pdf](notebook/Fixed_Wing_Surveillance_Drone_Project.pdf)
 
