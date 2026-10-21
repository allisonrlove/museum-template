---
title: Gallery
layout: default
date: 2026-01-01
summary: The whole collection seen at once, every object at its own proportions.
---

<div class="m-wide-wrap" style="margin-bottom:0" markdown="1">

<span class="m-kicker">Browse</span>

# Gallery

{: .lede}
The whole collection at a glance. Nothing is cropped to a common square: a tall scroll stays tall and a wide dish stays wide. Hover over a picture to read about it.

</div>

{% assign objects = site.pages
   | where_exp: "p", "p.path contains 'objects/'"
   | where_exp: "p", "p.path != 'objects.md'" %}

{% include nav/gallery-grid.html
  items=objects
  variant="masonry"
  min-width="240px"
  show-summary=true
  class="gallery-grid--bleed"
%}
