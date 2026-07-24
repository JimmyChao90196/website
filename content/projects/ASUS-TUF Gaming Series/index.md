---
title: "ASUS TUF Gaming Series"
date: 2026-05-05
description: "A commercial at Moonshine Animation for ASUS TUF. Smoke and RBD done in Houdini, brought into Unreal Engine via flipbook and vertex animation texture."
featureimage: "feature.webp"
tags: ["houdini", "unreal-engine", "commercial"]
showTableOfContents: true
showTaxonomies: true
---

{{< vimeo 785902134 >}}

## Overview

A commercial done at Moonshine Animation for ASUS TUF. The whole thing runs in Unreal Engine, but the effects were created in Houdini.

---

## My Contributions

| Effect | Pipeline |
|---|---|
| Smoke simulation | Houdini → flipbook → UE shader |
| RBD simulation | Houdini → vertex animation texture → UE |

---

## Breakdown

### Smoke

The smoke is done as a flipbook. I simulate it in Houdini, render out a sprite sheet of the frames, then set up a shader in Unreal that plays through them. It's not a real-time sim — Unreal is just playing back pre-rendered frames — but it looks convincing and runs fast.
<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="tuf-smoke-fast-fog.webp" alt="Fast moving fog and smoke swirling around the mech in close-up" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Fast fog</p>
  </div>
  <div>
    <img src="tuf-smoke-fog-valley.webp" alt="Wide foggy valley shot with the mech in the distance" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Fog valley</p>
  </div>
</div>

---

### RBD

The rock destruction is simulated in Houdini as a standard RBD sim, then baked out as a vertex animation texture (VAT). Houdini encodes the per-vertex position and normal data of every frame into a texture, then a shader in Unreal reads that texture and deforms the mesh accordingly. 

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="tuf-rbd-rock-hit.webp" alt="RBD simulation — rocks exploding outward as the mech stomps through the terrain" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">RBD - Simulation</p>
  </div>
  <div>
    <img src="tuf-rbd-explosion.webp" alt="Close-up of the RBD rock explosion with debris flying upward" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">RBD — Simulation</p>
  </div>
</div>

---

