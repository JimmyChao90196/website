---
title: "Shelf Toolkit Starter"
date: 2026-05-05
description: "A starter article for turning repeat Houdini actions into shelf tools."
featureimage: "img/mock/python.svg"
tags: ["python", "houdini", "shelf-tools"]
categories: ["Python"]
series: ["Python for Houdini"]
series_order: 1
showTableOfContents: true
showTaxonomies: true
---

This mock article is a place to collect repeatable Houdini shelf-tool patterns.

## Tool shape

### Inputs

Start with the selected nodes, current network editor, or active viewer state.

### Validation

Give clear messages when artists select the wrong node type.

### Output

Create nodes, add labels, and keep the network readable.

## Example skeleton

```python
import hou

nodes = hou.selectedNodes()
if not nodes:
    hou.ui.displayMessage("Select at least one node.")
```
