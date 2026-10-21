---
title: Objects
layout: default
date: 2026-01-01
summary: Every object in the collection. Filter by theme, or click any object to look closely.
---

<div class="m-wide-wrap" style="margin-bottom:0" markdown="1">

<span class="m-kicker">The collection</span>

# Objects

{: .lede}
Every object in the museum, from the oldest to the most recent additions. Choose a theme to narrow the wall, or click any object to see it up close.

</div>

{% assign objects = site.pages
   | where_exp: "p", "p.path contains 'objects/'"
   | where_exp: "p", "p.path != 'objects.md'" %}

{% include museum/object-grid.html items=objects %}
