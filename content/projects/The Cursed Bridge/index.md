---
title: "The Cursed Bridge"
date: 2026-06-03
description: "A movie at Moonshine Animation. I did the ghost wall effect and the glass shatter."
featureimage: "feature.png"
tags: ["houdini", "film", "vfx"]
showTableOfContents: true
showTaxonomies: true
---

{{< youtube vy9iq4OIfTU >}}

## Overview

All the VFX behind the scenes was done by **Moonshine Animation**. Big team on this one — I handled two effects: the ghost hands and faces coming out of the wall, and the glass shatter in the elevator.

---

## Ghost Hands & Faces Wall

Hands and faces pushing through a wall surface. Initially I wanted to achieve the effect without using Vellum simulation. Then I realized that having an extra layer of motion is pretty nice. So I ended up blending two things together.

![Houdini FX preview of the ghost wall geometry](cursed-bridge-fx-preview.png)

---

## Glass Shatter

This one I'm actually proud of. I built a procedural scatter system so the glass pieces are split into layers, and each layer has its own speed and spread. Not everything here is simulation though — a lot of the pieces are just forces, translation and rotation applied directly. Simple stuff, but it works and it gives you control.

The nice thing about having it layered is the director can ask for changes and you just turn a knob. Faster? Slower? Done. You're not re-doing the whole setup every time.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; margin:1.5rem 0;">
  <div>
    <img src="cursed-bridge-glass-shatter-full.png" alt="Glass exploding outward in the elevator" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Full glass explosion</p>
  </div>
  <div>
    <img src="cursed-bridge-glass-shatter-ceiling.png" alt="Looking up through layers of shattered glass" style="width:100%; border-radius:6px;"/>
    <p style="font-size:0.8rem; color:gray; margin-top:6px; text-align:center;">Looking up through the ceiling</p>
  </div>
</div>

The final comp with the actor below is the compositing team's work.

![Final comp with the actor — comp by the compositing team](cursed-bridge-glass-comp.png)
