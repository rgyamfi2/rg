# 🚕 London Drive — Free Roam

A browser-based, free-roam driving game set in a stylised **London**, built with
[Three.js](https://threejs.org/) (real-time 3D). Hop in a black cab and cruise a
grid of city streets past landmarks like **Big Ben**, the **London Eye**,
**St Paul's Cathedral**, the **Shard**, and the **Gherkin** — with red buses,
black cabs, phone boxes, street lamps, parks and pedestrians all around.

No installs, no build step. It's a single self-contained page — Three.js is
vendored into the repo, so it runs straight from a URL.

## ▶️ Play

Once GitHub Pages is live (one-time setup below), open:

**https://rgyamfi2.github.io/rg/**

## 🎮 Controls

| Action | Keys |
| --- | --- |
| Accelerate | `W` / `↑` |
| Brake / reverse | `S` / `↓` |
| Steer | `A` `D` / `←` `→` |
| Handbrake (slide) | `Space` |
| Change camera | `C` |
| Horn | `H` |
| Reset car | `R` |

On phones/tablets, on-screen touch buttons appear automatically.

Cameras cycle through **Chase → Cinematic → Bonnet → Bird's-eye**. A live
**minimap** (top-right) shows the street grid, traffic, and landmark markers,
and place names pop up as you approach each landmark.

## 🌐 Publishing (GitHub Pages) — one-time setup

GitHub won't let automation switch Pages on for the first time, so flip this
one setting yourself (takes ~30 seconds, only ever needed once):

1. Open the repo on GitHub → **Settings** → **Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Set **Branch** to `claude/london-freeroam-game-xaqk00` and folder to
   **`/ (root)`**, then click **Save**.
4. Wait ~1 minute, then open **https://rgyamfi2.github.io/rg/**.

That's it — the game is live at that URL and you can share it with anyone.
A `.nojekyll` file is included so GitHub serves the files exactly as they are.

## 🛠 Tech

- **Three.js r160** (vendored at `vendor/three.module.js` — no CDN dependency)
- Procedural city grid, instanced road markings, PBR-ish materials, soft shadows,
  a gradient sky dome and distance fog
- Arcade car physics (speed-sensitive steering, handbrake slides, collisions)
- Pure ES modules + an import map — nothing to compile

Everything is in `index.html`.
