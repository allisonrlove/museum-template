---
title: Exhibitions
layout: default
date: 2026-01-01
summary: Themed rooms that gather objects and essays around one idea.
---

<div class="m-wide-wrap" style="margin-bottom:0" markdown="1">

<span class="m-kicker">Visit the rooms</span>

# Exhibitions

{: .lede}
An exhibition is a room built around one idea. Each gathers a handful of objects from across the collection, puts them in a deliberate order, and says why they belong together.

</div>

{% assign rooms = site.pages
   | where_exp: "p", "p.path contains 'exhibitions/'"
   | where_exp: "p", "p.path != 'exhibitions/index.md'" %}

{% include museum/exhibition-grid.html items=rooms %}
