Project Workflow
1. Geometry Cleanup & Domain Setup
The geometry consists of a multi-body part with two distinct domains to establish a fluid-solid interface:
• Fluid Domain (rec): A rectangular channel enclosure housing the solid body.
• Solid Domain (cylinder): A cylinder positioned normal to the flow path.
• Topology: Non-manifold topology shared using the Share Topology feature in DesignModeler to ensure perfect conformal mesh mapping at the fluid-solid zone interface.
2. Mesh Generation
A high-quality mesh was generated using the native Fluent Watertight Geometry meshing pipeline:
• Mesh Type: Poly-Hexcore (Mosaic technology) combining a structured hex core with polygonal surface inflation layers.
• Sizing Controls: Local face sizing applied at the cylinder-fluid interface to resolve the thermal and hydrodynamic boundary layers.
• Boundary Layers: Prism inflation layers added along the walls and cylinder interface to maintain a low \(y^{+}\) value.
3. Boundary Conditions
The physics configuration utilizes the following boundary conditions:
• Inlet: velocity-inlet with a uniform velocity profile and specified inlet temperature (300 K).
• Outlet: pressure-outlet maintaining atmospheric gauge pressure
• Outer Wall: wall bounding the rectangular channel.
• Fluid-Solid Interface: Automatic coupled wall zone mapping both heat flux and temperature fields continuously across boundaries.
4.Results and Post-Processing
Fluid-Solid Temperature Distribution
The temperature fields were evaluated using volume rendering and planar cross-sections in CFD-Post:
• Volume Rendering: Illustrates the thermal wake developing directly downstream of the heated solid body as energy transfers into the fluid domain.
• Temperature Contours: Show a high-temperature zone concentrated near the stagnation point and developing thermal boundary layers along the flanks of the cylinder.
Velocity Streamlines
• Streamlines seeded at the inlet display regular flow acceleration around the cylinder obstruction.
• The flow path captures velocity deficit regions and wake development immediately downstream of the cylinder, highlighting the correlation between flow separation zones and localized convective heat transfer coefficients.
