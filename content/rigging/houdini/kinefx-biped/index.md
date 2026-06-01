---
title: "KineFX Biped Blockout"
date: 2026-05-09
description: "A note about KindFX in Houdini"
featureimage: "img/mock/rigging.svg"
tags: ["rigging", "houdini", "kinefx"]
categories: ["Rigging"]
series: ["Rigging for Houdini"]
series_order: 1
showTableOfContents: true
showTaxonomies: true
---

## Overview
Overall kineFX has few traits, just like what we would expected in other 3D software, but slightly different in it's own way.
- Joints: They are presented as points and lines in Houdini, which is quite interesting to be honest.
- Skinning: Establishing up weight.
- Rig: If a parent joint is moved, the children joint is affected as well.
- Procedural Control: You can even use vex and vop for rigs. Rigs are sops!

## Skeleton pass

### Joint layout

Start with a readable hierarchy and stable naming.

### Control pass

Create simple controls that prove animator intent before adding detail.

### Deformation pass

Test the minimum skinning setup needed for feedback.

## Notes

Keep the first pass boring and easy to debug.
