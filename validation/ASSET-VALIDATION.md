# Local model validation

This is evidence from local preparation, not a supplied test implementation.

- Model: championship-ring.glb
- Bytes: 550,344
- Version: 87870ccab314
- Meshes: 14
- Triangles: 149,788
- Body triangles: 131,320
- Lid triangles: 18,468
- Hidden triangles: 0
- Materials: Body metal, Recessed gold, Cast metal
- Container and compression: GLB 2.0, KHR_draco_mesh_compression
- External images/textures: none

The source validator decoded the actual model and checked its hash/version, required nodes, bounds, zones, parts and sampled text charts. All three focused suites passed, with 37 tests. Type checking, lint and a production webpack build passed in the separate local validation application. Blender 5.1.2 opened the master and imported the GLB. A browser rendered HARPER, CAPTAIN and 07 on the actual shoulder.

The validation application, test sources, scripts and dependencies are outside swsb. Full browser/accessibility coverage, a clean reader installation and runtime skill discovery remain unverified. This report grants no redistribution rights.
