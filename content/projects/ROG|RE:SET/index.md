---
title: "ROG | RE:SET"
date: 2026-05-10
description: "A commercial VFX project I worked on at Moonshine Animation — fireworks, lightning, particles, smoke, and a few effects I'd never tried before."
featureimage: "img/mock/project.svg"
tags: ["houdini", "commercial"]
showTableOfContents: true
showTaxonomies: true
---

{{< youtube m0ScSSMANkg >}}

## Overview

This is a commercial cinematic I worked on at **Moonshine Animation** for ASUS Republic of Gamers. The story is set in this gritty cyberpunk racing world — neon signs, destroyed cities, a crowd losing their minds in an arena. Good vibes.

My job was the FX. Every spark, explosion, lightning arc, and fireworks burst you see in this video came from Houdini. It was one of the more intense projects I've done — tight deadlines, a lot of effects, and most of them needed to look good in the same frame without stepping on each other.

Here's what I was responsible for:

- Rainbow effect
- Fireworks & particle simulation
- Smoke simulation
- Lightning effect
- Pixelation effect
- Comp in Nuke

---

## Breakdown

### Rainbow Effect

This one shows up on the big live screen in the arena — a wave of colour sweeping across as the crowd reacts. The world has this very neon, over-the-top aesthetic so the effect needed to feel loud and saturated. Matching the energy of the scene without looking out of place was the main challenge here.

![Rainbow streaks on the live broadcast screen in the arena](rog-rainbow-effect.png)

---

### Fireworks & Particle Simulation

There are two fireworks moments. The first is a dense particle trail cascading down the race track — a wall of purple embers that needed to feel heavy and physical. The second is the hero shot: the ROG logo igniting in the sky. That one had to be readable at distance, which meant a lot of tuning on the burst shapes.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="rog-particle-fireworks.png" alt="Purple particle trail falling across the race track" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Particle trail on the track</p>
  </div>
  <div>
    <img src="rog-fireworks-logo.png" alt="ROG logo shape formed by fireworks bursting in the night sky" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">ROG logo fireworks — the hero beat</p>
  </div>
</div>

---

### Lightning Effect

Honestly this was the trickiest part. Lightning runs through several shots — tight on the character's face, then wide over a ruined city, then back in close during a fight. The hard thing with lightning is it can easily look random and cheap. You want it to feel intentional, like it has weight and direction. A lot of the work was in the seeding and damping to get shapes that actually read well on screen.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="rog-lightning-character.png" alt="Red energy crackling around the character's face in close-up" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Energy surge — character close-up</p>
  </div>
  <div>
    <img src="rog-lightning-highway.png" alt="Blue lightning bolts striking across a highway at speed" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Lightning on the highway</p>
  </div>
</div>

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="rog-lightning-burst.png" alt="Lightning burst exploding outward in an urban environment" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Lightning burst in the city</p>
  </div>
  <div>
    <img src="rog-lightning-arc.png" alt="Lightning arc stretching across the sky above a ruined cityscape" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Wide city shot — lightning arc</p>
  </div>
</div>

---

### Speed & Pixelation Effect

The speed effect is pretty much just making you feel like you're inside the race — radial blur, streaking light, the whole thing. The pixelation effect is more of a stylistic device that fits the ROG brand language, that digital-glitch look they use a lot. Both of these ended up being quicker to nail than the lightning, which was a relief.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="rog-speed-effect.png" alt="Radial speed blur with purple and blue streaking light" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Speed effect</p>
  </div>
  <div>
    <img src="rog-pixelation-effect.png" alt="Pixelation and light beam effect in a post-apocalyptic city" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Pixelation effect</p>
  </div>
</div>

---

## Reflection

Looking back, the biggest thing I took from this project is that FX work in a commercial pipeline is a different kind of pressure than personal projects. You're not just making something that looks cool — it has to look cool, fit the shot, match the comp, and be done by tomorrow. That combination pushes you to work faster and make decisions with less iteration than you'd normally allow yourself.

The lightning was where I spent most of my time, and it's also what I'm most proud of in this piece. Getting those arcs to feel deliberate and art-directed rather than random — that's the whole game with lightning in Houdini.
