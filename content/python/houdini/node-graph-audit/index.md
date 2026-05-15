---
title: "Node Graph Audit"
date: 2026-05-06
description: "A mock checklist for scanning Houdini networks before publishing."
featureimage: "img/mock/python.svg"
tags: ["python", "houdini", "pipeline"]
categories: ["Python"]
series: ["Python for Houdini"]
series_order: 2
showTableOfContents: true
showTaxonomies: true
---

Use this as a future home for scripts that find bypassed nodes, missing labels, broken references, and heavy caches.

## Audit targets

### Naming

Check whether important nodes follow the expected prefix and suffix rules.

### Dependencies

Report missing files, absolute local paths, and disabled cache nodes.

### Performance

Flag expensive nodes before the publish step.

## Output format

Start with a simple table: node path, severity, message, and suggested action.
