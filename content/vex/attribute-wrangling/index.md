---
title: "Attribute Wrangling Basics"
date: 2026-05-01
description: "A starter module for points, primitives, groups, and naming conventions in VEX."
featureimage: "img/mock/vex.svg"
tags: ["vex", "houdini", "attributes"]
categories: ["VEX"]
series: ["VEX Foundations"]
series_order: 1
showTableOfContents: true
showTaxonomies: true
---

This placeholder article shows the article-level structure: series block, tags, and an outline generated from Markdown headings.

## Goal

Create predictable attributes that downstream nodes can read without extra cleanup.

## Core ideas

### Attribute classes

Use point attributes for per-point behavior, primitive attributes for per-face decisions, and detail attributes for shared settings.

### Naming pattern

Mock convention:

```c
f@fx_mask = clamp(@Cd.r, 0.0, 1.0);
s@module = "hero_scatter";
```

## Practice task

Build a small wrangle that creates `fx_mask`, `variant_id`, and `module` attributes from a test grid.
