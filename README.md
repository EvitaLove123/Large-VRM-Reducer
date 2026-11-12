# Large VRM Reducer

Browser-side VRM inspection and VRM 0.x Secondary Animation metadata helper.

## Current first version
- Opens GLB binary files (.vrm and .glb).
- Reads GLB 2.0 JSON and reports file size, node count, and skin-joint count.
- For an existing VRM 0.x file, detects likely secondary bones by existing joint names (hair, skirt/cloth, tail, ears/wings, accessories).
- Adds VRM 0.x `extensions.VRM.secondaryAnimation.boneGroups` while preserving existing groups by default.
- Exports a new `.vrm` file without changing the original.
- All processing happens locally in the browser.

## Important limitations
- A plain GLB is not converted into VRM by this helper. It must first be exported as a valid VRM by a separate GLB-to-VRM exporter.
- VRM 1.0 `VRMC_springBone` is not written by this first version.
- No bones are invented. Detection depends on meaningful names and skin joints.
- No colliders are fabricated. Auto-generated groups use conservative defaults; tune physics/colliders in a compatible editor when needed.
- Texture/mesh compression is not implemented yet; the app does not claim to reduce file size in this version.

## Run
Enable GitHub Pages for the repository and use the root `index.html`.
