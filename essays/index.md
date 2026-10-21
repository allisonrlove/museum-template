---
title: Essays
layout: default
date: 2026-01-01
summary: Long-form essays that follow an idea across the collection.
---

<div class="m-wide-wrap" style="margin-bottom:0" markdown="1">

<span class="m-kicker">Reading room</span>

# Essays

{: .lede}
An object page describes one thing. An essay follows an idea through several of them, and says what the collection knows that no single object can.

</div>

{% assign essays = site.pages
   | where_exp: "p", "p.path contains 'essays/'"
   | where_exp: "p", "p.path != 'essays/index.md'" %}

{% include museum/essay-grid.html items=essays %}
