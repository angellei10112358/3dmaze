# 3D Maze (maze3d.html)

A single-file first-person 3D maze game. Double-click `maze3d.html` to play in any modern browser (Chrome / Edge / Firefox / Safari) — no build step, no npm, works over `file://` or any static server.

## How to play

- Find the glowing green exit beacon to win.
- **Move:** `WASD` / arrow keys · **Look:** mouse (click the scene to lock the pointer)
- **Run:** `Shift` · **Minimap:** `M` · **Hint (+30s):** `H`
- **Retry same maze:** `R` · **New maze:** `N` · **Pause:** `Esc`
- Mobile: left stick to move, drag the right half of the screen to look.
- Same maze, same seed: share a URL like `?seed=12345&size=15` to replay it.

## Features

- Seeded random maze generation (iterative DFS backtracker + extra loops), exit placed at the BFS-farthest cell
- Three difficulty levels: 8×8, 15×15, 25×25
- Single-draw-call walls (`InstancedMesh`), procedural Canvas textures, fog, flashlight-style lighting
- Circle-vs-AABB collision with wall sliding, fog-of-war minimap, per-difficulty best times (`localStorage`)
- Hint route, WebAudio footstep/win sounds, head bob

## Tech

- Only external dependency: Three.js `0.160.0` via CDN importmap (version pinned). No other libraries, images, fonts, or audio files.
