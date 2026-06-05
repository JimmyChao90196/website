---
title: "ROG | Strix SCAR"
date: 2026-05-15
description: "A commercial at Moonshine Animation for ASUS ROG. I did the smoke simulation, liquid magnet geometry deformation, and particle swipe effect."
featureimage: "feature.webp"
tags: ["houdini", "commercial"]
showTableOfContents: true
showTaxonomies: true
---

{{< vimeo 794029395 >}}

## Overview

Another commercial done at **Moonshine Animation** for ASUS ROG.

---

## My Contributions

| Effect |
|---|
| Smoke simulation |
| Geometry deformation — liquid magnet effect |
| Particle swipe |

---

## Breakdown

### Liquid Magnet Effect

No simulation here. Just vector manipulation — the geometry deforms toward the hand using distance-based math, and you get spikes that follow the finger across the surface. There's also a liquid ripple that spreads outward around the contact point, which adds a lot to the feel of it. The whole thing reads like ferrofluid but there's no sim running under the hood, which keeps it fast and easy to art-direct.

![Close-up of the liquid magnet effect — geometry spiking up as a hand touches the surface](strix-scar-liquid-magnet.webp)

---

### Smoke Simulation

![Wide shot of the smoke simulation with red laser beams crossing through it](strix-scar-smoke-sim.webp)

---

### Particle Swipe

Dense field of glowing cube particles sweeping through the scene. The main thing to get right is the directionality. A particle swipe that just appears randomly reads as noise. You want it to feel like it's going somewhere.

![Character surrounded by the particle swipe — dense blue and purple cube particles filling the frame](strix-scar-particle-swipe.webp)
