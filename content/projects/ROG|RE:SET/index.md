---
title: "ROG | RE:SET"
date: 2026-05-10
description: "A commercial VFX project produced at Moonshine Animation — particle simulations, lightning, fireworks, and stylized effects for the ROG RE:SET cinematic."
featureimage: "feature.png"
tags: ["houdini", "commercial"]
showTableOfContents: true
showTaxonomies: true
---

{{< youtube m0ScSSMANkg >}}

## Overview

**ROG | RE:SET** is a commercial cinematic produced at **Moonshine Animation** for ASUS Republic of Gamers. 

My role focused entirely on the **VFX side**: designing and simulating the effects that punctuate the key story beats. Sparks, lightning strike, every burst of fireworks in this piece went through Houdini.

---

## My Contributions

| Effect | Tool |
|---|---|
| Rainbow effect | Houdini |
| Fireworks & particle simulation | Houdini |
| Smoke simulation | Houdini |
| Lightning effect | Houdini |
| Pixelation effect | Houdini |

---

## Breakdown

### Rainbow Effect

The rainbow streaks appear on the live broadcast screen during the crowd sequence — a wave of colour washing over the arena as the crowd reacts. The effect needed to feel vibrant and slightly surreal to match the cyberpunk aesthetic of the world.

![Rainbow effect streaking across the live broadcast screen](rog-rainbow-effect.png)

---

### Fireworks & Particle Simulation

Two distinct fireworks moments in the spot. The first is a dense particle trail cascading down the race track — millions of purple embers filling the frame. The second is the hero beat: the ROG logo igniting in the sky as a fireworks burst, a centrepiece shot that needed to read clearly even at distance.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="rog-particle-fireworks.png" alt="Pixelation effect" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Particle trail — race track sequence</p>
  </div>
  <div>
    <img src="rog-fireworks-logo.png" alt="ROG logo formed in fireworks bursting in the night sky" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">ROG logo fireworks — hero beat</p>
  </div>
</div>

---

### Lightning Effect

The lightning runs through several shots — from close on the character's face as energy crackles around him, to wide city shots where arcs tear across the skyline. Houdini's wire solver was used to drive the branching behaviour, keeping it physically believable while still being stylised enough to read as supernatural.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="rog-lightning-character.png" alt="Red energy and lightning crackling around the character's face" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Character close-up — energy surge</p>
  </div>
  <div>
    <img src="rog-lightning-highway.png" alt="Blue lightning bolts striking across a highway during a race" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Lightning on the highway</p>
  </div>
</div>

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="rog-lightning-burst.png" alt="Lightning burst exploding outward in a destroyed urban environment" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Lightning burst — urban combat</p>
  </div>
  <div>
    <img src="rog-lightning-arc.png" alt="Lightning arcing across the sky above a ruined cityscape" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Lightning arc — wide city shot</p>
  </div>
</div>

---

### Speed & Pixelation Effect

The speed effect gives the racing sequences their sense of raw velocity — a radial blur with streaking light that places the camera right inside the action. The pixelation effect is used as a stylistic transition, echoing the digital-glitch visual language of the ROG brand.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="rog-speed-effect.png" alt="Radial speed blur with purple and blue light streaks" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Speed effect — race sequence</p>
  </div>
  <div>
    <img src="rog-pixelation-effect.png" alt="Pixelation and light beam effect in a ruined cityscape" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Pixelation effect — transition</p>
  </div>
</div>

---

## Reflection

This was one of the more demanding commercial projects I've worked on — tight deadlines, high visual bar, and a lot of effects needing to coexist in the same frame without fighting each other. The biggest challenge was the lightning: making branching arcs feel intentional and art-directed rather than random. A lot of iteration went into the seeding and damping parameters to get the shapes to read well on screen.

Working in Houdini for simulation and handing off to Nuke for compositing was a smooth pipeline, and it was satisfying to see effects that started as point clouds and wire solvers end up in a polished commercial.
